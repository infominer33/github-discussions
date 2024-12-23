---
title: "Simplify abstract data model to be more concrete"
date: 2024-07-01 13:07:19 +0000
author: msporny
excerpt: >
  This was discussed during the [#did meeting on 20 November 2024](https://www.w3.org/2024/11/20-did-minutes.html#5e18).  
  <details><summary><i>View the transcript</i></summary>  
  <h3><a href=\"https://github.com/w3c/did-core/issues/855\" rel=\"noopener noreferrer\">w3c/<wbr>did-core#855</a></h3>
  <p><cite>decentralgabe:</cite> The topic of today is issue 855, simplify abstract data model to be more concrete.</p>
  <p><cite>decentralgabe:</cite> Manu opened the issue, Joe has made some comments, invite either one of you to queue to speak to the issue and what you'd like to see happen in the group.</p>
  <p><cite>JoeAndrieu:</cite> I made my case in the Github issue, the abstract data model is a bad idea (my opinion), some think it's a good idea. My biggest problem is that its untestable and was not tested in last iteration, avoided raising that last time, political difficulties was why we avoided the discussion. We have spec features that are not implemented, we need to fix that.</p>
  <p><cite>manu:</cite> I agree that the abstract data model doesnt buy us much in this spec<br>
  <span>… I agree we didnt push on it last iteration due to other challenges being worked through the group</span><br>
  <span>… I disagree that we have untestable features in the spec. Perhaps JoeAndrieu can point these out</span><br>
  <span>… One of the biggest problems is the amount of time that we as a group spend talking about it</span><br>
  <span>… As a spec editor I don;t know how much work it would take to remove the abstract data model. I am fairly confident it wouldn't affect implementations</span><br>
  <span>… Perhaps a signal that the abstract data model isnt buying us much</span><br>
  <span>… Also noting that the controller document does not have an abstract data model. So it will be a little strange to use a base document with a concrete data model - the controller doc - then layer on an abstract data model</span><br>
  <span>… I think the biggest danger with removing the abstract data model, is  to do with the amount of effort we put in to make the DID spec abstract. I think we did a good job here</span><br>
  <span>… removing the abstract data model will invite a couple of things. People will throw their hands up and say well DIDs are not for me. And go off an do DID like things elswhere</span><br>
  <span>… There may be knock on effects from this change that we will have to deal with. This could take 2-3 months of our time</span><br>
  <span>… Also noting this could happen anyway due to the adoption of the controller doc</span><br>
  <span>… I am on the fence of the way forward</span></p>
  <p><cite>decentralgabe:</cite> I want to highlight point about practical DID adoption - focus groups time on impactful time on objectives.</p>
  <p><cite>markus_sabadello:</cite> I started with reason for abstract data model -- some wanted DID Documents in JSON-LD and plain JSON and that's obsolete already if we adopt controller document and I think we already had a resolution on one media type -- application/did -- both JSON and JSON-LD, interpretation would be the same whether there is a context, whether or not you use JSON-LD processor, interpretation is the same... with that, I'm thinking, why do we need an<br>
  <span>… abstract data model still? Doesn't that remove original rationale/reasoning?</span></p>
  <p><cite>ivan:</cite> I was one arguing for abstract data model, still believe in it, that being said, I think most important point at this time is the controller document work -- my understanding, the DID Document and data model is a controller document with some minor features. Probably it's a bit extreme, but most of DID Core spec related to DID Document would be removed form standard anyway, in a sense, controller document might have made this entire discussion moot by</p>
  <p>now.</p>
  <p><cite>decentralgabe:</cite> We might need more analysis on controller document impact? Is that a good next step?</p>
  <p><cite>ChristopherA:</cite> I've been in favor of abstract model, in reality, it has now become a signal rather than a technical reality... there are a number of parties that will take removing it as a signal of 100% in on JSON-LD and that there are people will object to that, whether that's relevant or they're implementing DIDs, I don't know. Might cause us headaches.</p>
  <p><cite>bigbluehat:</cite> Verifiable Credentials does JSON and JSON-LD without an abstract data model.</p>
  <p><cite>manu:</cite> responding to ChristopherA, the text in current controller doc is not JSONLD maximalist. It says we would like you to include a context, but does not require it<br>
  <span>… I have the same concerns as ChristopherA, people will twist this to their narrative that we are JSONLD only. When in fact we have gone the other way. <code>@context</code> is not required, but it is one way to signal to version of the spec you are using</span><br>
  <span>… What we want to say is that the semantics are the same between a JSONLD and JSON documents. If they are not this is a mistake. That is currently in the spec</span><br>
  <span>… I don't think it has any implementation issues with removing the abstract data model</span><br>
  <span>… What we could do is say we are going to remove the abstract data model and see who raises their voices to challenge this direction</span><br>
  <span>… There may be statements that were helpful to us that we were getting ready to remove. We are not allowed to make class 4 changes. There might be arguments that this is a class 4 change. But I think we can work around it</span><br>
  <span>… We are lucky that the test suite tests against concrete instantiations of the data model. Getting rid of the ADM is not going to affect the test suite</span><br>
  <span>… We could do a pass to remove the abstract data model and see if doing that changes any normative changes. Then we could say we are doing this, point at what the new thing looks like and then wait for the reaction of the community</span></p>
  <p><cite>decentralgabe:</cite> A proposal to align DID Core with Controller Document to see what normative changes it might make and gauge reaction from community.</p>
  <p><cite>markus_sabadello:</cite> I'm not so worried about political reactions, <code>@context</code> is effectively optional, which was the original desire of people that just wanted to do plain JSON. They didn't say they wanted abstract data model, they didn't want abstract representations, they wanted <code>@context</code> to be optional, and that's what we have right now. Spec would be less complex, another benefit (people say it's complicated). I'm not that concerned about the reactions.</p>
  <p><cite>&lt;Zakim&gt;</cite> JoeAndrieu, you wanted to mention political pushback was based on a misunderstanding that JSON-LD is not JSON</p>
  <p><cite>ivan:</cite> Yeah, I think I'll proposal something along the line of what Manu proposed: In view of controller document, and we decided to align, we can essentially declare the issue about abstract data model as moot -- no need to keep discussing, we will rely on controller document most of the time, whole thing will disappear without referring to it. It will just go away, automatically, we don't have to discuss it anymore, which creates energy loss.</p>
  <p><cite>JoeAndrieu:</cite> That's interesting Ivan, I like that thinking, I do think as we shift to controller document, it has a concrete representation, we have to extract between two... won't make sense to make controller document abstract.</p>
  <p><cite>JoeAndrieu:</cite> One of the reasons I'm not too concerned w/ political fallout, based on misunderstanding on JSON-LD vs. JSON -- people thought they were two different things, we can have common representation that both world views can accept current state.</p>
  <p><cite>ChristopherA:</cite> If we had a non-CBOR-LD version of controller documents, boutique one, that we might show you can have other formats that we support. Don't see anyone on this call that is comitted to boutique CBOR representation, to demonstrate we're abstract instead of putting in the spec.</p>
  <p><cite>Wip:</cite> The controller document argument is compelling, but this group needs to pass a resolution to adopt it, I think we were waiting for it to go into next stage of W3C Process.</p>
  <p><cite>Wip:</cite> What is our story around allowing alternate formats? CBOR, YAML, etc? I think thing there is same as VCDM, people have to define bidirectional map from their representation into JSON. There should be a pathway for people to implement DID Documents in whatever way they want.</p>
  <p><cite>decentralgabe:</cite> Chair hat off: Other representations, does it close the door on non-JSON representations, solved elsewhere?</p>
  <p><cite>&lt;Zakim&gt;</cite> JoeAndrieu, you wanted to mention alternate formats</p>
  <p><cite>&lt;ivan&gt;</cite> <a href=\"https://github.com/w3c/did-core/issues/854\" rel=\"noopener noreferrer\">Issue on the reference to the Controller Document</a></p>
  <p><cite>JoeAndrieu:</cite> I think it makes it easier, in current pattern, what we have is other representations -- go back to abstract data model, you have to go to abstract data model, which they didn't do in the first place. What we want is to go between serializations, anything is valid as long as you go from X to DID Document, then people can compress it ... it's just not a DID Document (yet), as long as you have a transformation that can get you back to the<br>
  <span>… original, you're fine.</span></p>
  <p><cite>JoeAndrieu:</cite> If we start w/ abstract data model, it's more difficult, if we don't, it's easier to deal w/ alternate representations.</p>
  <p><cite>&lt;Zakim&gt;</cite> manu, you wanted to comment on demonstrating CBOR</p>
  <p><cite>manu:</cite> +1 to what JoeAndrieu &amp; Wip said. We have language around being conformant with the DID document ecosystem. With bidirectional transformation rules. I agree with JoeAndrieu's point that without the ADM this is easier. As long as people can convert their representation into the DID doc representation you are golden.<br>
  <span>… for example in YAML it is very straightforward. There are many libraries that transform YAML into JSON.</span><br>
  <span>… If people want to do compression, they can do that. So long as you can get back to the original representation. You wouldnt have to worry about the abstract data model</span><br>
  <span>… hearing a lot of consensus</span><br>
  <span>… I did think we already passed a resolution about using the controller document.</span></p>
  <p><cite>&lt;ivan&gt;</cite> <a href=\"https://github.com/w3c/did-core/issues/854#issuecomment-2332954287\" rel=\"noopener noreferrer\">Latest comment on the relationship to the CD</a></p>
  <p><cite>manu:</cite> It is stable enough that the editors could make an attempt to alight the DID core spec with the controller document and remove the ADM. Seeing if we run into any normative changes that are required<br>
  <span>… What do we think are the next steps</span></p>
  <p><cite>decentralgabe:</cite> We did pass resolution to align w/ controller document when we're ready. I'm good to not pass another one, just have Editor's do the work. If people feel that's not strong enough, we need a resolution, happy to run one if someone wants to draft the language.</p>
  <p><cite>markus_sabadello:</cite> I agree with Manu and Joe, one thing I was wondering, does it affect extension properties in any way? it's a good thing to do that, how would that change if we don't have abstract data model? Would we require people to register their extensions in our registry? Still optional?</p>
  <p>FYI I do not see a resolution about adopting the controller document here - <a href=\"https://www.w3.org/2024/list-resolutions/?g=did\" rel=\"noopener noreferrer\">https://<wbr>www.w3.org/<wbr>2024/<wbr>list-resolutions/?g=did</a></p>
  <p><cite>burn:</cite> I added myself to queue before Manu -- this is basically an extended +1, about the direction we're talking about moving -- you had questioned this Markus, when I put first draft of spec into ReSpec, talked w/ Manu about this, I abstracted out from the specific syntax and try to create generic model and concrete realizations.</p>
  <p><cite>burn:</cite> That was for two reasons -- it was very clear there was going to be a battle around JSON vs. JSON-LD -- this is the Verifiable Credentials spec -- other reason, we did want to make it clear to people was say that what we were trying to define wasn't limited to specific syntax, used XML as an example -- we've gradually removed XML and other things. This conversation has convinced me, as Manu said, there is another way to address challenges for original<br>
  <span>… abstract data model was meant to address.</span></p>
  <p><cite>burn:</cite> As a proponent for the abstract data model (historically), I think arguments have been addressed correctly, we did same thing w/ DID spec because of what happened w/ VC spec, it's time to move on, thanks for all the great work!</p>
  <p><cite>&lt;ivan&gt;</cite> <a href=\"https://www.w3.org/2024/09/05-did-minutes.html#t04\" rel=\"noopener noreferrer\">Latest discussion in the group on the controller issue</a></p>
  <p><cite>ChristopherA:</cite> General statements are: we can remove abstract syntax model if we do X, but then when I hear the list it includes things that are \"oh, well it needs to be two way -- what does that mean?\" Gordian can do elision and it will look just like a DID Document, conformant there, but Gordian-specific one that understands elision is a superset of capabilities and it isn't two way. One interpretation of two-way, along with this, we don't have to use<br>
  <span>… abstract syntax model, but we do need other points on what's going to replace that, better definition of what does round-trip really mean? It's not clear to me.</span></p>
  <p><cite>ivan:</cite> I did some digging, I put pointers to minutes, last time we discussed this in WG, they all go in same direction - we didn't have a formal resolution, good to have it, agreement of WG to wait until CR.</p>
  <p><cite>&lt;Zakim&gt;</cite> manu, you wanted to talk to registration of extensions</p>
  <p><cite>manu:</cite> ChristopherA asked a good question. Wondering if we can defer answering what we mean by two way map until we are able to make a editorial pass.<br>
  <span>… Would like us to pass a proposal around the general direction and let the editors discover any issues that arise from this. We want to make Gordian work with DIDs, but we need to figure out how to do this.</span><br>
  <span>… With respect to markus's registration question. I think this is the same thing. We want extensions to be able to happen, and do not want to make drastic changes. But concerned that trying to solve these now will derail us. Would prefer to get started with the work and let that teach us</span><br>
  <span>… decentralgabe with respect to your proposal, lets leave out until CR. What is left on the controller document is largely editorial. Would like to start sooner than later on this</span></p>
  <p><cite>decentralgabe:</cite> Ok, I've updated the proposal, we need to figure out two-way transformations, other representations, and how extensions are managed. I would like to see the group agree to try to address these after, open to hear what everyone thinks.</p>
  <p><cite>JoeAndrieu:</cite> I had proposed something incomplete, we don't control the controller document, we can't remove abstract data model from controller document -- a wrinkle -- proposal from Gabe is good, didn't have it depend on CR. I would also like to get into resolution on concrete representation for DID Document.</p>
  <p><cite>decentralgabe:</cite> Maybe we can split into two resolutions?</p>
  <p><cite>JoeAndrieu:</cite> I'm ok with two resolutions.</p>
  <p><cite>decentralgabe:</cite> will run proposal after Markus.</p>
  <p><cite>markus_sabadello:</cite> I agree with dealing w/ technical details after running resolution.</p>
  <p><cite>&lt;decentralgabe&gt;</cite> PROPOSAL: Align DID Core with the Controller Document specification (<a href=\"https://www.w3.org/TR/controller-document/\" rel=\"noopener noreferrer\">https://<wbr>www.w3.org/<wbr>TR/<wbr>controller-document/</a>), and attempt to remove language around the Abstract Data Model.</p>
  <p><cite>manu:</cite> +1</p>
  <p><cite>&lt;burn&gt;</cite> +1</p>
  <p><cite>&lt;ivan&gt;</cite> +1</p>
  <p><cite>&lt;JoeAndrieu&gt;</cite> +1</p>
  <p><cite>&lt;markus_sabadello&gt;</cite> +1</p>
  <p><cite>&lt;Wip&gt;</cite> +1</p>
  <p><cite>&lt;TallTed&gt;</cite> +1</p>
  <p><cite>&lt;dmitriz&gt;</cite> +1</p>
  <p><cite>&lt;bigbluehat&gt;</cite> +1</p>
  <p><cite>&lt;danpape&gt;</cite> +1</p>
  <p><cite>&lt;JennieM&gt;</cite> +1</p>
  <p><cite>&lt;ChristopherA&gt;</cite> +0</p>
  <p><cite>&lt;ChristopherA&gt;</cite> (pending other proposal)</p>
  <p><strong>RESOLUTION:</strong> Align DID Core with the Controller Document specification (<a href=\"https://www.w3.org/TR/controller-document/\" rel=\"noopener noreferrer\">https://<wbr>www.w3.org/<wbr>TR/<wbr>controller-document/</a>), and attempt to remove language around the Abstract Data Model.</p>
  <p><cite>&lt;ChristopherA&gt;</cite> reshare draft?</p>
  <p><cite>decentralgabe:</cite> ok, on to the second proposal from Joe.</p>
  <p><cite>ChristopherA:</cite> Is this the one where we can put in bidirectional transformation and interpretation of concrete representation, maybe? Extension and intent to support other formats. That's not in this proposal.</p>
  <p><cite>JoeAndrieu:</cite> I'll try to wordsmith the proposal.</p>
  <p><cite>manu:</cite> I think we need to be more specific. The controller document is very clear about it being JSON. The DID document should be just as clear</p>
  <p><cite>&lt;ivan&gt;</cite> +1 to manu. We have to be aligned with the CD</p>
  <p><cite>&lt;burn&gt;</cite> I suggest avoiding the word \"serialization\" and instead use \"representation\" or \"syntax\"</p>
  <p><cite>manu:</cite> THis doesnt mean that it is the only representation. It is totally okay to have a CBOR representation. There are multiple levels. One is there is a JSON representation, if it follows all the rules you are good to go. The other is if you can get whatever representation you want into the concrete JSON representation then you are good to go<br>
  <span>… I an hesitant about getting that language into this proposal</span><br>
  <span>… Lets leave the bidirectional language out of it for now</span><br>
  <span>… Then we wait to see if people in the community have issues with that.</span></p>
  <p><cite>&lt;JoeAndrieu&gt;</cite> good for me</p>
  <p><cite>decentralgabe:</cite> Let's say we allow alternative representations and come up with that language later.</p>
  <p><cite>markus_sabadello:</cite> Probably missing something, why do we need to profile this, why is this not part of profile document that we reference?</p>
  <p><cite>JoeAndrieu:</cite> We don't control the controller document, we don't know what it'll end up as.</p>
  <p><cite>markus_sabadello:</cite> We reference it, we will use it, profile it in a way -- why would profile have anything w/ representation -- JSON vs. JSON-LD? Controller document, how to use context, etc.</p>
  <p><cite>JoeAndrieu:</cite> language i\"m trying to get in -- expect other specs to profile controller document, serialization might be something we don't like. I don't think it'll go in that direction, but if we're dependent on that gorup, we have to profile it anyway, we have things in DID Core that have to do w/ that document.</p>
  <p><cite>JoeAndrieu:</cite> If controller document changes, we would have to undo that in our profiling.</p>
  <p><cite>&lt;Zakim&gt;</cite> manu, you wanted to note it has to do w/ media type.</p>
  <p><cite>manu:</cite> I agree with JoeAndrieu. We dont currently specify a media type in the controller document. This has to do with media types. The DID spec will have a different media type to the controller document<br>
  <span>… I dont think it hurts to include this in the proposal</span></p>
  <p><cite>decentralgabe:</cite> Does that clarify, Markus? Ok with language?</p>
  <p><cite>markus_sabadello:</cite> Sure, don't fully understand but not against, please run the proposal.</p>
  <p><cite>&lt;decentralgabe&gt;</cite> PROPOSAL: When profiling the Controller Document for the DID Document specification we will use JSON as a concrete representation, with language describing options for alternative representations.</p>
  <p><cite>&lt;manu&gt;</cite> +1</p>
  <p><cite>&lt;JoeAndrieu&gt;</cite> +1</p>
  <p><cite>&lt;ivan&gt;</cite> +1</p>
  <p><cite>&lt;Wip&gt;</cite> +1</p>
  <p><cite>&lt;markus_sabadello&gt;</cite> +0.5</p>
  <p><cite>&lt;ChristopherA&gt;</cite> +1 (and revises my previous +0 to +1)</p>
  <p><cite>&lt;bigbluehat&gt;</cite> +1</p>
  <p><cite>&lt;JennieM&gt;</cite> +1</p>
  <p><cite>&lt;danpape&gt;</cite> +1</p>
  <p><cite>&lt;decentralgabe&gt;</cite> +1</p>
  <p><cite>&lt;dmitriz&gt;</cite> +1</p>
  <p><strong>RESOLUTION:</strong> When profiling the Controller Document for the DID Document specification we will use JSON as a concrete representation, with language describing options for alternative representations.</p>
  <p><cite>decentralgabe:</cite> We need to ensure controller document has media type, we'll have to raise that issue over there.</p>
  <p><cite>&lt;ChristopherA&gt;</cite> Ciao!</p>  
  <hr /></details>
categories: w3c
tags: did-core
comments_file: did-core-issue-855_comments
permalink: /did-core/855/
url: https://github.com/w3c/did-core/issues/855
last_modified_at: 2024-11-20 15:56:18 +0000
---


**URL:** https://github.com/w3c/did-core/issues/855

It has been suggested that the abstract data model in DID Core creates unnecessary complexity and that a more concrete data model should be selected, based on implementation experience over the past two years. This issue is to track the discussion of how that simplification might occur.