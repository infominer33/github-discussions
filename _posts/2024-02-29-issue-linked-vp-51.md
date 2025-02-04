---
title: "Add AI transcription to WG meetings"
date: 2024-02-29 08:54:34 +0000
author: ankurdotb
excerpt: >
  This is ready for review and discussion of next steps. This was much trickier to integrate than I thought, so some details as well (for posterity).  
  ## Summary
  Here's a summary of the changes and resulting functionality
  - Enabled AI summaries by default at the account level: this means all new meetings will get this setting
  - Backfilled this setting for old meetings
  - Added a new \"Summaries\" sheet within the DIF Meeting Recordings spreadsheet ([here](https://docs.google.com/spreadsheets/d/1wgccmMvIImx30qVE9GhRKWWv3vmL2ZyUauuKx3IfRmA/edit?gid=1289343804#gid=1289343804))
  - Created a Google AppScript that queries for new meeting summaries from Zoom meeting summaries API. It does the following:
      - Gets new meeting summaries
      - For each new meeting summary, populates \"Summaries\" sheet
      - Creates human-readable google doc for each. This is filed by meeting series, under [DIF Meetings > Meeting Summaries](https://drive.google.com/drive/folders/1FMyMB-zDLWIlnQat4XK00JwLbFbuHykL?usp=drive_link), and linked from the Summaries sheet  
  ## To Discuss
  - [ ] Cleaning up transcription errors
      - There are clearly errors (as expected) in the AI transcription. 
      - We could give permission for TSC chairs to edit the docs, but is this now an obligation?
      - **Proposed**: insert text that this is AI-generated and hasn't been reviewed. Chair can remove it when they're editing
      - Side note: if we are editing the doc, this would argue for dropping the spreadsheet columns with this data, or automate back-propagating (but that might be overly tedious to keep the same structure, so I believe the former is better)
  - [ ] \"Integrating\" the Summaries data with the rest of the spreadsheet
      - **Proposed**: change new meeting entries in the [Recordings spreadsheet](https://docs.google.com/spreadsheets/d/1wgccmMvIImx30qVE9GhRKWWv3vmL2ZyUauuKx3IfRmA/edit?gid=0#gid=0) to link to a google folder containing all meeting materials (recording, summary, transcript, ...)
      - See details below about why & tradeoffs
  - [ ] FYI, I intend to postpone the following due to the time required for this so far.
      - Backfilling meeting summaries (i.e. piping old recordings to a ai summary tool)
      - Moving zoom recordings to google drive (zoom cloud storage costs us $100/mo, but effort to do that makes it lower priority)  
  
  ## Details  
  ### Fetching Meeting Summaries
  Zapier's zoom integration didn't work correctly for meeting summaries. Note: I'm not exactly sure why; they have a meeting summary event, which should function similarly to our \"new meeting recording\" event, but Zapier logs (plus google searches) didn't give me the visibility I needed.  
  Therefore, I used the Zoom API and created a Google App Script. It fetches all new available (non-empty) meeting summaries as of the last query date (per the last entry in a spreadsheet)  
  - Query uses a `from` param as the last \"meeting start time\" in the Summaries sheet (plus 1 minute so it doesn't refetch)
  - Post-fetch filters out meetings with summary start time of Unix epoch beginning (the signal that it will be empty)
  - Adds newly available summaries to the Summaries sheet. 
      - Each summary object has metadata, overview, details, and next steps. Those are stored as columns in a row
      - The summary object is also converted to a human-readable google doc, which is created and linked from column C
  - This script is visible to those with administrative access 
  - I didn't want to expose the google appscript via an open REST endpoint, so it's not called by Zapier. Instead, it triggers on a daily timer  
  ### Integrating Summaries into Recordings spreadsheet  
  The link to zoom-stored recordings shows pieces of the summary, but it's tedious to navigate, and I assume people would like the summary in complete text form. So the question is how to reconcile meeting recording links and summary links.  
  Originally, I'd assumed we would link the meeting summaries next to the recording link in the Recordings spreadsheet. But the current structure of the Recordings spreadsheet makes it extremely tedious to add a new column.   
  A further complication is that the meeting recordings objects in zapier do not integrate summaries. We could manually match (post-fetching) on meeting + datetime substring, but we'd then need to propagate that to the Recording sheet and through all Working group + work item sheets.  
  IMO the best solution is what I proposed above, i.e. create meeting instance folders in google drive, put the recording + summary (and whatever else) in there, and link to that folder from the spreadsheet. Here's how it would work:
  - Since we have to deviate from Zapier anyway for summaries, we could switch off current zaps that link the recordings spreadsheet to the zoom cloud-stored recording
  - Update my google appscript to download recordings in addition to summary
  - In the recording spreadsheet, link to a folder containing the recording, summary, and other data (detailed transcript)
  - Then the working group + work item sheets automatically get the updated values  
  This means we get all of the good behavior going forward (not using zoom cloud storage for new meetings, spreadsheet links to all meeting materials).  
  The downsides are:  
  1.  there's a cutoff point of Dec 16, 2024 so we'd have before-and-after behavior. I.e., afterward, these entries (in pink, **Figure 1**) would link to a DIF google folder containing recording, summary, transcript, etc, instead of linking to the zoom cloud recording. 
  2. The zoom cloud recording link built-in player is more user-friendly than the google drive media player.  
  Other alternatives considered:
  1.  just link to the meeting series share near the header. This avoids needing to adjust columns, but does not have a direct meeting instance to summary link. See **Figure 2**. This is easy, but lame
  2. Overhaul this spreadsheet approach. Too much work, but can consider later  
  
  **Figure 1:**
  <img width=\"992\" alt=\"Image\" src=\"https://github.com/user-attachments/assets/5539438d-0d75-4a9d-a485-c54af843ea4d\" />  
  **Figure 2:**
  ![Image](https://github.com/user-attachments/assets/c790a3a9-c7a3-4d1b-8b3a-81e5eaf3aa01)  
categories: decentralized-identity
tags: linked-vp
comments_file: linked-vp-issue-51_comments
permalink: /linked-vp/51/
url: https://github.com/decentralized-identity/linked-vp/issues/51
last_modified_at: 2024-12-28 20:24:51 +0000
---


**URL:** https://github.com/decentralized-identity/linked-vp/issues/51

@kimdhamilton Is it possible to activate an AI meeting notetaker at Zoom account level so that it automatically takes notes? Would people be comfortable meetings being recorded and/or having an AI notetaker?