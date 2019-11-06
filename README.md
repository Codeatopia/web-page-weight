# web-page-weight
WiP - Application to measure the network usage of a website

# Why webpage weight?
This repo is the product of diving waaay to far down a black hole ahead of a presentation on the carbon impact of the interent.
Tools exist already to measure the size of a webpage (notably https://www.websitecarbon.com/), however the common way to do this by looking at the response size of http requests which will often fail to pick up on async loaded images, videos etc.

Another notable project is https://github.com/aberforthQ/puppeteer-split-test, which uses puppeteer to visit actual sites and record data transferred metrics. This is a much better indicator, although still doesn't give the full picture as sizes are non-compressed (? - tbc)

Chrome's own developer tools has a bunch of metrics which include total network transferred (compressed and uncompressed), however this information doesn't appear to be exposed to 3rd party services, see:
- https://github.com/GoogleChrome/puppeteer/issues/667
- https://github.com/ChromeDevTools/devtools-protocol/issues/12

This tool will aim to find away to extract the information found in devtools network tab
