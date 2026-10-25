---
layout: post
title: Do you track liquidation scenarios in your startup?
date: '2011-02-01T08:23:46'
slug: do-you-track-liquidation-scenarios-in-your-startup
permalink: /do-you-track-liquidation-scenarios-in-your-startup/
categories:
- Uncategorized
tags:
- case studies
- deals
- due diligence
- law
- risk management
- tips
excerpt: Fred Wilson has had a series of posts relating to M&A transactions, generally
  revolving around case studies. This one on ChiliSoft describes how certain features
  embedded in the capitalization table (liquidation preferences and floating price
  warrants), coupled with being acquired for shares rather than cash led to a seemingly
  dramatic erosion of value for the…
---

Fred Wilson has had a series of posts relating to M&A transactions, generally revolving around case studies. This one on [ChiliSoft](<http://avc.com/2011/01/ma-case-studies-chilisoft/>) describes how certain features embedded in the capitalization table (liquidation preferences and floating price warrants), coupled with being acquired for shares rather than cash led to a seemingly dramatic erosion of value for the target shareholders.

The key point here is not whether any particular structure is “right” for every transaction. The point actually is that your CFO, or your lawyer if he knows how to work a spreadsheet, should keep track of your capitalization table and what it means. The “what it means” part is, in my experience, best done graphically, depicting the payouts to various groups of holders at different liquidation prices. (In every set of venture documents I’ve seen, a merger or acquisition is treated as a liquidation.) That depiction has to take into account conversions, exercises, and the conditions and triggers that cause them.

My best story about this issue comes not from an M&A transaction per se, but from a set of unusual liquidation preferences I read in a term sheet. The terms included different multipliers at various thresholds, and something about the text didn’t make sense to me. I checked with the venture associate (who had actually been a corporate lawyer at my old firm) to confirm. The answer back was “yep, that’s what we want.” I have a habit of being too smart for my own good sometimes, and so I didn’t take the client’s answer for a given (frankly, that’s not my job — my job is to get it as right as possible). Instead, I did the only thing that made sense to me — show that the terms were somehow wrong. (NB: the meta-lesson here is that reading terms like these, particularly when they are complex, and certainly when you are reading several sets of terms in conjunction with one another, is really damn hard.) I chose to do that with Excel.

I put together a relatively simple graph, showing the total value of the company vs. the share for common and series A (or B or whatever it was) holders. The answer became obvious: the language as written operated to give the new investors, less money as the company became more valuable from $200m to $300m (or something like that). That never makes any sense. Keeping their share static, or shifting the share different ways, all could make sense and provide distinct incentives to management: but taking money out of anyone’s pocket in that scenario makes no sense.

[![]({{ '/assets/uploads/2011/01/Liquidation-waterfall.jpg' | relative_url }})](<{{ '/assets/uploads/2011/01/Liquidation-waterfall.jpg' | relative_url }}>)

I’ve left it unedited and uncleaned (the axes are atrocious, the legend is back in excel, etc.) because all you have to do is look at those two vertical lines at $211m and $240m company valuation and see the problem.

This type of analysis doesn’t have to happen on a daily basis; it’s not a dashboard item. But in the middle of, meaning before signing, any capital raise or other issuance of equity, you’d better have one of these from your CFO. Or your banker. Or your venture consultant. Or your lawyer (and if your lawyer doesn’t know how to do this in excel, [call one who does](<http://rickcolosimo.com>)). When skilled venture-firm folks can make these mistakes, it’s certain that company management does too.
