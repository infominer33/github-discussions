---
title: "URI in Profile triggers CORS Unsafe Request Header Byte rule"
date: 2024-06-24 21:08:08 +0000
author: azaroth42
excerpt: >
  This was discussed during the [json-ld meeting on 13 November 2024](https://www.w3.org/2024/11/13-json-ld-minutes.html#bb35).  
  <details><summary><i>View the transcript</i></summary>  
  <h3>Issue Discussion</h3>
  <p><cite>bigbluehat:</cite> We're working through the project list.</p>
  <p><cite>gkellogg:</cite> added issues that are class 1-3.</p>
  <p>subtopic <a href=\"https://github.com/w3c/json-ld-syntax/issues/436\" rel=\"noopener noreferrer\">w3c/json-ld-syntax#436</a></p>
  <p><cite>&lt;gb&gt;</cite> <strong><a href=\"https://github.com/w3c/json-ld-syntax/issues/436\" rel=\"noopener noreferrer\">Issue 436</a></strong> URI in Profile triggers CORS Unsafe Request Header Byte rule (by azaroth42) [spec:w3c] [needs discussion] [tag-needs-resolution]</p>
  <p><cite>gkellogg:</cite> might just create \"tokens\" for profile paraemters.</p>
  <p><cite>gkellogg:</cite> tokens not being namespaced is mitigated by the fact that the media-type is the namespace.</p>
  <p><cite>bigbluehat:</cite> So, it treats the media-type as the namespace.<br>
  <span>… Profile parameters not having a colon is wide-reaching</span></p>
  <p><cite>gkellogg:</cite> not sure how we update guidance for using profile parameters.</p>
  <p><cite>bigbluehat:</cite> This would be a breaking change for web annotations.<br>
  <span>… That would mean web annotations needs their own media type.</span></p>
  <p><cite>niklasl:</cite> dlehn's reply may mean this isn't as horrible as it seems.<br>
  <span>… I think the datasets working group has done something with this.</span></p>
  <p><cite>pchampin:</cite> This doesn't seem to be a problem where things can't work, but making them work is tricky, due to pre-flight requests.<br>
  <span>… If we expect a server to support profile-based content-negotiation, it doesn't come automatically.</span><br>
  <span>… If you want to support this, you'll also need to support pre-flight requests.</span></p>
  <p><cite>&lt;bigbluehat&gt;</cite> q|</p>
  <p><cite>pchampin:</cite> This is difficult to configure and easily forgotten.</p>
  <p><cite>&lt;gb&gt;</cite> <strong><a href=\"https://github.com/w3c/json-ld-syntax/issues/436\" rel=\"noopener noreferrer\">Issue 436</a></strong> URI in Profile triggers CORS Unsafe Request Header Byte rule (by azaroth42) [spec:w3c] [needs discussion] [tag-needs-resolution]</p>
  <p><cite>bigbluehat:</cite> There were some suggestions for defining enumerated values (tokens).</p>
  <p><cite>&lt;pchampin&gt;</cite> I think it wouldn't hurt to define \"short names\" for the profiles in addition to the currently defined IRIs</p>
  <p><cite>bigbluehat:</cite> The key is to not make it a breaking change.<br>
  <span>… This would affect the media-type registration.</span></p>
  <p><cite>niklasl:</cite> Aren't link headers defined similarly, where there are pre-defined tokens and IRIs may also be used.</p>
  <p><cite>bigbluehat:</cite> Browsers have made decisions which are affecting what we can do.</p>
  <p><cite>&lt;bigbluehat&gt;</cite> &gt; When processing the \"profile\" media type parameter, it is important to note that its value contains one or more URIs and not IRIs. In some cases it might therefore be necessary to convert between IRIs and URIs as specified in section 3 Relationship between IRIs and URIs of [RFC3987].</p>
  <p><a href=\"https://www.w3.org/TR/json-ld11/#iana-considerations\" rel=\"noopener noreferrer\">https://<wbr>www.w3.org/<wbr>TR/<wbr>json-ld11/#iana-considerations</a></p>
  <p><cite>&lt;niklasl&gt;</cite> application/ld+json;profile=\"<a href=\"http://iiif.io/api/presentation/3/context.json\" rel=\"noopener noreferrer\">http://<wbr>iiif.io/<wbr>api/<wbr>presentation/<wbr>3/<wbr>context.json</a>\"</p>
  <p><cite>niklasl:</cite> I think it would be good to add tokens. Rob's specific problem are more about the other uses of profiles.<br>
  <span>… I wonder if our solution would be considered a solution for the issue; maybe parts of the issue can't be solved in the JSON-LD spec. Might recommend IIIF to use profile negotiation.</span><br>
  <span>… But, using pre-flight does work, so that would be on their end.</span><br>
  <span>… It's more that we put forward the design pattern and it has become more tricky.</span></p>
  <p><cite>bigbluehat:</cite> The ramifications of this are not just expand/compact/... Rob's point is for other specifications that used the same pattern.<br>
  <span>… No we know to avoid it.</span></p>
  <p><cite>&lt;niklasl&gt;</cite> See also: <a href=\"https://www.w3.org/TR/dx-prof-conneg/\" rel=\"noopener noreferrer\">https://<wbr>www.w3.org/<wbr>TR/<wbr>dx-prof-conneg/</a> (and <a href=\"https://profilenegotiation.github.io/I-D-Profile-Negotiation/I-D-Profile-Negotiation.html\" rel=\"noopener noreferrer\">https://<wbr>profilenegotiation.github.io/<wbr>I-D-Profile-Negotiation/<wbr>I-D-Profile-Negotiation.html</a> )</p>
  <p><cite>bigbluehat:</cite> There's reason to document this in the best-practices document. How this affects other specs would mean that they cannot treat profile as being extensible, and will need a new media type.</p>
  <p><cite>gkellogg:</cite> we might create a registry to allow other specifications to add their profile parameters without needing a new media-type.</p>
  <p><cite>bigbluehat:</cite> niklasl shared a document on using the profile parameter for content negotiation.</p>
  <p><cite>pchampin:</cite> Reaching out the that TAG would be a good idea, as other specs rely on this, and they would be impacted.<br>
  <span>… I'd like to see their thoughts and how much we should make the effort to try to change this.</span><br>
  <span>… Regarding the spec, note that this is a working draft which has been inactive for a while. This might not be the strongest argument to take before the TAG. (The dataset exchange WG)</span><br>
  <span>… Part of the reason that spec is stalled is that there are contentious discussions with IETF on where it belongs.</span></p>
  <p><cite>&lt;niklasl&gt;</cite> From the dx-prof-conneg draft: During 2018, DXWG members had a longer discussion with the JSON-LD WG at the annual forum TPAC in Lyon, France and it was concluded that the \"profile” parameter in the Accept and Content-Type headers should be seen to convey profiles that are specific to the Media Type [such as JSON-LD's expanded  .... ]</p>
  <p><cite>pchampin:</cite> But, is there enough interest in IETF to continue the work?</p>
  <p><cite>niklasl:</cite> There are aspects of the draft that goes into the profile parameter of the media type is the right way to go.<br>
  <span>… The design of IIIF and Activity Streams I appreciate more when not looking at it from an RDF perspective.</span><br>
  <span>… These are more useful at the intersection of JSON and RDF, which makes it easier to create specifications in a distributed way.</span><br>
  <span>… If I believed (from RDF perspective) that format is irrelevant, general content negotiation works well.</span><br>
  <span>… I can see how the TAG might argue from one of these perspectives. Maybe we shouldn't invent media-types on the fly.</span></p>
  <p><cite>&lt;pchampin&gt;</cite> <a href=\"https://www.w3.org/TR/vc-data-model-2.0/#media-type-precision\" rel=\"noopener noreferrer\">https://<wbr>www.w3.org/<wbr>TR/<wbr>vc-data-model-2.0/#media-type-precision</a></p>
  <p><cite>pchampin:</cite> Regarding the value of using JSON-LD media-type with parameter vs a new media-type, VC has had to rely on this for a while.<br>
  <span>… The current solution is to have a dedicated media-type with additional language to explain the relationship between the two media types.</span><br>
  <span>… We might point other specs to that solution.</span></p>
  <p><cite>&lt;niklasl&gt;</cite> +1 to mentioning that \"third\" point of view (very pertinent IMHO)</p>
  <p><cite>bigbluehat:</cite> I think we need to move on and come back to this issue.<br>
  <span>… It would be great to write some of these things up on the issue so that we have something coherent to bring to the TAG.</span><br>
  <span>… IETF has shifted their approach, and we're stuck in the middle. In the mean time, if we can collect thoughts in the issue.</span><br>
  <span>… I don't think we know enough to lay out the preferred solution.</span><br>
  <span>… If we go the short-name route, we run the risk of turning into a registry.</span></p>
  <p><cite>&lt;bigbluehat&gt;</cite> <a href=\"https://github.com/w3c/json-ld-syntax/issues/443\" rel=\"noopener noreferrer\">w3c/<wbr>json-ld-syntax#443</a></p>
  <p><cite>&lt;gb&gt;</cite> <strong><a href=\"https://github.com/w3c/json-ld-syntax/issues/443\" rel=\"noopener noreferrer\">Issue 443</a></strong> `@protected` creates unresolvable conflicts when the same term is defined in two contexts top-level (by trwnh) [spec:editorial] [wr:commenter-agreed-partial] [class-2]</p>  
  <hr /></details>
categories: w3c
tags: json-ld-syntax
comments_file: json-ld-syntax-issue-436_comments
permalink: /json-ld-syntax/436/
url: https://github.com/w3c/json-ld-syntax/issues/436
last_modified_at: 2024-11-13 17:59:49 +0000
---


**URL:** https://github.com/w3c/json-ld-syntax/issues/436


In the IANA registration [1], we define a media type parameter called 'profile'. Its value is a space separated list of URIs, for which we registered six initial values. These can be composed together, and new values can be added for other "constraints or conventions".

The IIIF specifications use this functionality, for example to define the specific structure of the response in an API [2] as part of the media type. Similarly in Linked Art, we do the same [3].

However, in the WHATWG specification for fetch [4], it says that the *value* for the Accept header is NOT CORS safe, if it has more than 128 bytes (which multiple URIs might easily cause) or (more importantly) if the value contains an unsafe header byte. The unsafe header bytes include the character ":" ... which prevents *any* URI or CURIE with a namespace prefix separate by : from being CORS safe. 

This means that we cannot use the JSON-LD media type as registered for content negotiation via the `accept` header according to the fetch specification, which was much of the rationale for the profile parameter.

To resolve this, either WHATWG would need to change fetch, or W3C/IANA would need to change the definition of the media type and give some registration function for possible `profile` values, then all downstream specifications would need to register a safe profile value to use.

I've added the tag-needs-resolution label, as I think that's the level this would need to run up to :(

[1] https://www.w3.org/TR/json-ld11/#iana-considerations
[2] https://iiif.io/api/presentation/3.0/#63-responses 
[3] https://linked.art/api/1.0/json-ld/#introduction
[4] https://fetch.spec.whatwg.org/#ref-for-cors-unsafe-request-header-byte
