---
title: Following up on HTML innovation vs maintenance
layout: page
---

I think there is some misunderstanding about what problems we’re trying to solve from the recent discussions between the browser engine vendors and W3C.

## The future of HTML

W3C is the natural custodian for HTML. We need to come together as a community as W3C participants to decide how we will manage, maintain, and develop HTML in the coming years. In the last few years, the HTML Working Group has focused almost solely on completing HTML 5.0 and publishing a Recommendation. At the same time the amount of new technical work in the group has diminished. The level of engagement, especially from browser vendors who write much of the software that exposes the capabilities of HTML, has fallen to a very low level.

The challenge before us is how to reengage the community to continue maintenance of HTML 5.0 and to bring and develop new functionality. The [various](http://darobin.github.io/after5/html-plan.html) [versions](http://w3c.github.io/charter-html/html-plan.html) of the HTML Plan have presupposed that we need a HTML Working Group to accomplish this. The discussions we’ve had about the plan have centred around who should chair this group and what new features might we work on in HTML.

## What problems are we trying to solve?

At Microsoft, we feel that the pain points for our engagement at W3C are broader than simply what to do with the HTML Working Group and throughout this process we’ve tried to take a step back and address the broader points.

The three highest priority issues that we want to solve are:
  * How to incubate new ideas with low friction
  * How to make faster progress on stabilising standards and getting to Recommendation
  * How to update and maintain specifications when we find interop issues

### Incubating new ideas

We want to incubate new ideas with the lowest friction possible while we figure out if they are good ideas and if they have support from the broader community. We want to have these discussions with a well understood contribution license so that we can take the good ideas forward onto the Recommendation track.

There appears to be strong consensus for the creation of the Web Platform Incubator Community Group to address this issue for new features. We have a few process issues to resolve but we are in good shape here.

### Making faster progress on stabilising specifications

We want to make faster progress on getting standards stabilised and to Recommendation status. Today we have many specifications languishing in LC/CR stage because we have some tests in a test suite for which we don’t have two passes. This isn’t preventing web developers from using the features but it is blocking progress on specifications.

We clearly need to get the balance right here. We don’t want to standardise something where the specification isn’t complete enough to accomplish interoperability. We do not want to postpone interoperability on new features until we see problems in the field. On the other hand, if multiple browsers have broadly implemented these features and they are in use on many web sites without a large number of reported problems then we shouldn’t block progress of the specification.

We haven’t yet agreed on how to do this.

### Updating Recommendation to support better interop

Despite it taking a long time to get specifications to Recommendation status, our engineering team frequently finds issues where a web site behaves differently in different browsers because a standard doesn’t the correct behaviour or because one or more browsers didn’t follow the spec. In these cases we want to work together to either agree to change our implementations to match the spec or to update the spec with new language.

Today we don’t have a good process that is well-understood to accomplish this in most working groups.

In addition, as we discussed “legacy interop” we didn’t have agreement about how to approach this. Take the URL spec as an example. At Microsoft we are aiming to fix the interoperability gaps with URL processing that are affecting real web sites. Sam Ruby has a comprehensive test suite that shows dozens of differences between browsers but for us resolving these isn’t a high priority. We have a large backlog of work we want to do and we don’t detect that people are running into these issues very often. I heard other people expressing the view that they would want to take advantage of the hard work Sam has done and close out those differences sooner regardless of the immediate impact to developers. Eventually these differences will bite someone so we should address them now since someone has done the legwork.

Most likely we’ll need to address this type of discussion on a case by case basis. There will be no one size fits all.

## Applying this to HTML

At Microsoft have two priorities when it comes to HTML.

First and foremost we want to make sure there is a venue to do maintenance of HTML 5.0 when we detect interop issues affecting web developers and causing web sites to behave differently between browsers.

Secondly we want to understand how to propose small new ideas that make minor enhancements to HTML. For substantial new features we will propose them as extension specifications into the Web Platform Incubator group. We don’t yet understand how to propose minor tweaks.

At TPAC 2014, I heard overwhelming support for modularisation of HTML moving ahead. On the other hand, we have a HTML 5.1 specification that has substantial new features incorporated in it as a monolithic document. 

## To recharter a HTML Working Group or not?

The argument that I have heard for rechartering the HTML Working Group goes as follows: HTML is a fundamental part of the web platform. We all agree that HTML is not “done”. We need somewhere to do maintenance of HTML 5.0. In our discussions we heard some ways in which we might extend HTML. Philippe has collected [other ideas in his HTML Plan](http://w3c.github.io/charter-html/html-plan.html#directions). It seems logical therefore to charter the HTML Working Group to own this maintenance and to host this new work on HTML.

One problem I see is that there is a difference between a set of things that people **could** work on and the set of things that are in a high enough priority that they **will** work on them in the next 12 months. At Microsoft we don’t have a long list of features we want to add to HTML in the next year.

Part of our goal was to reinvigorate the work around HTML and to get the community to re-engage. I have talked to several people who were sceptical that they would find the HTML Working Group an inviting place to do new work based on past history. We have discussed what it would take to overcome this including whether we might need new working group chairs. Another aspect we’ve discussed is that we need to lead by example. If each of the browser engine vendors identifies people to participate and makes a commitment to show up and engage then we stand a good chance of winning back the wider community who want to work with us.

My worry is that there isn’t enough work to do just doing maintenance on HTML 5.0 and while we have some ideas for new work we could do we don’t know that anybody actually wants to work on them in the next 12 months. If we relaunch the working group but then do no work will we accomplish our goal? I think we only get once chance to do this so we need to have confidence that it will work.

It is for this reason that I’ve asked us to consider whether we should do HTML work in a different working group. If we put HTML maintenance work alongside other work we know people want to actually do then perhaps we can be more successful. My suggestion has been characterised as merging HTML and WebApps but that is just one option and perhaps there are other alternatives.

The list of deliverables in WebApps is huge and varied. Perhaps we should rationalise them. As a thought experiment what if we had the following working groups:

  * **Web Core** – including HTML, DOM, UI Events, Selection, Clipboard, Editing, URL, WebIDL, IME, etc.
  * **Storage and Networking** – including IndexedDB, Push API, XHR, File API, File System API, Service Workers, Packaging, Manifest, Quota, Streams, etc.
  * **Web Components** – Shadow DOM, Custom Elements, HTML Imports, data binding, etc.
  * **Media** – EME, MSE, transcript, track binding, etc.

This would be quite disruptive but I just want to start the discussion with out assuming that the only plan should be to recharter HTML. This is a rough proposal I came up with in a few minutes. I'm sure there are other better alternatives.
