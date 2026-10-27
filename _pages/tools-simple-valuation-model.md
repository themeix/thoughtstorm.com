---
layout: page
title: Simple Valuation Model
slug: simple-valuation-model
permalink: /tools/simple-valuation-model/
---

<h2 class="text-2xl sm:text-3xl font-serif text-[#29385b] font-normal mb-6">Introductory Valuation Tool</h2>

<p class="mb-5 text-[18px] leading-relaxed text-[#424242]">Here's a simplified valuation framework extracted from financial models and valuations we've built for clients over the years. You start by adding some summary financial information from your projections. If you plug in the numbers from your financial model, it'll give you a quick view of how those numbers affect the valuation of the company from a VC perspective. There are possibly a few more blanks on the sheet than might fit your company, but that's the constraint of having a tool that you can use this way.</p>

<p class="mb-5 text-[18px] leading-relaxed text-[#424242]">Once the company's financial projections are added, you will see that those numbers are used in two ways, which are then combined to describe a valuation range.</p>

<ol class="list-decimal pl-6 mb-6 space-y-3 text-[18px] leading-relaxed text-[#424242]">
  <li>We take the sum of cash flows and discount them back to present value.</li>
  <li>We look at the final year of projections and use the numbers to calculate two different valuations: one based on a revenue multiple and one based on earnings.
    <ul class="list-disc pl-6 mt-2 space-y-2 text-[17px]">
      <li>The multiples have to be adjusted for a specific business and market, but the current values are very broad defaults. There are specific spots in the sheet to add comparable companies. By calculating their values for P/E and P/Rev, you can add support to your use of particular multiples in the analysis – but only to the extent that the companies are actually comparable.</li>
    </ul>
  </li>
  <li>We add the discounted cash flows to an average of the P/E and P/Rev terminal values to create a range of possible values.
    <ul class="list-disc pl-6 mt-2 space-y-2 text-[17px]">
      <li>The array is there because you need to understand that valuation is seldom just one number because there are too many embedded assumptions further up the page.</li>
    </ul>
  </li>
</ol>

<p class="mb-5 text-[18px] leading-relaxed text-[#424242]">The ultimate valuation is also greatly dependent on a particular investor's discount rate and expected return. We've included some basic standards by showing how an expected multiple of return over five years converts to a discount rate. So, if a VC expects a 3x return in five years, that equates to a 25% discount rate. Why this approach? Because while I've never seen a VC write or talk about their fund's discount rate, I've often seen them describe multiples they like to aim for (recognizing, when they're sober, that the 100x return is much like a black swan and one they really can't expect to recognize in advance because markets work).</p>

<p class="mb-6 text-[18px] leading-relaxed text-[#424242]">Let us know if you have any questions.</p>

<div class="w-full overflow-x-auto my-8 border border-gray-200 shadow-sm bg-white p-2 sm:p-4">
  <iframe src="{{ '/assets/uploads/Tools/Valuation/formvald17th.htm' | relative_url }}" name="frame1" class="w-full border-0" style="min-width: 720px; max-width: 950px; height: 1950px;" frameborder="0" scrolling="no"></iframe>
</div>
