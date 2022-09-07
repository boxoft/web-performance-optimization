# Web Performance Optimization

## Contents

1. Introduction

- [What is web performance?](https://developer.mozilla.org/en-US/docs/Learn/Performance/What_is_web_performance)

  - > **Web performance** is the objective measurement and perceived user experience of a web site or application.
  - > This includes the following major areas:
    >
    > - Reducing overall load time
    > - Making the site usable as soon as possible
    > - Smoothness and interactivity
    > - Perceived performance
    > - Performance measurements

- [The "why" of web performance](https://developer.mozilla.org/en-US/docs/Learn/Performance/why_web_performance)
  - > **Web performance** refers to how quickly site content loads and renders in a web browser, and how well it responds to user interaction.

2. RAIL and Metrics

- The [RAIL](https://web.dev/rail/) Model
  > - Response: process events in under 50ms
  > - Animation: produce a frame in 10 ms
  > - Idle: maximize idle time
  > - Load: deliver content and become interactive in under 5 seconds
- [User-centric Performance Metrics](https://web.dev/user-centric-performance-metrics/)

  - [Web Performance Working Group](https://www.w3.org/webperf/)
  - [Important metrics to measure](https://web.dev/user-centric-performance-metrics/#important-metrics-to-measure)
    > - [First Contentful Paint (FCP)](https://web.dev/fcp/)
    > - [Largest Contentful Paint (LCP)](https://web.dev/lcp/)
    > - [First Input Delay (FID)](https://web.dev/fid/)
    > - [Interaction to Next Paint (INP)](https://web.dev/inp/)
    > - [Time to Interactive (TTI)](https://web.dev/tti/)
    > - [Total Blocking Time (TBT)](https://web.dev/tbt/)
    > - [Cumulative Layout Shift (CLS)](https://web.dev/cls/)
    > - [Time to First Byte (TTFB)](https://web.dev/ttfb/)

3. Lighthouse and Chrome DevTools

- [Lighthouse](https://web.dev/lighthouse-performance/)

  - Performance audit scoring
    > - [Lighthouse performance scoring](https://web.dev/performance-scoring/)
  - Metrics
    > - [Speed Index](https://web.dev/speed-index/)
  - Opportunities
    > - Eliminate render-blocking resources
    > - Properly size images
    > - Defer offscreen images
    > - Minify CSS
    > - Minify JavaScript
    > - Remove unused CSS
    > - Efficiently encode images
    > - Serve images in modern formats
    > - Enable text compression
    > - Preconnect to required origins
    > - Reduce server response times (TTFB)
    > - Avoid multiple page redirects
    > - Preload key requests
    > - Use video formats for animated content
    > - Reduce the impact of third-party code
    > - Avoid non-composited animations
    > - Lazy load third-party resources with facades
  - Diagnostics
    > - Avoid enormous network payloads
    > - Serve static assets with an efficient cache policy
    > - Avoid an excessive DOM size
    > - Avoid chaining critical requests
    > - User Timing marks and measures
    > - Reduce JavaScript execution time
    > - Minimize main thread work
    > - Ensure text remains visible during webfont load
    > - Keep request counts low and transfer sizes small

- [Chrome DevTools](https://developer.chrome.com/docs/devtools/)

  - [Chrome DevTools](https://web.dev/rail/#chrome-devtools)
    > - Throttle your CPU to simulate a less-powerful device.
    > - Throttle the network to simulate slower connections.
    > - View main thread activity to view every event that occurred on the main thread while you were recording.
    > - View main thread activities in a table to sort activities based on which ones took up the most time.
    > - Analyze frames per second (FPS) to measure whether your animations truly run smoothly.
    > - Monitor CPU usage, JS heap size, DOM nodes, layouts per second, and more in real-time with the Performance Monitor.
    > - Visualize network requests that occurred while you were recording with the Network section.
    > - Capture screenshots while recording to play back exactly how the page looked while the page loaded, or an animation fired, and so on.
    > - View interactions to quickly identify what happened on a page after a user interacted with it.
    > - Find scroll performance issues in real-time by highlighting the page whenever a potentially problematic listener fires.
    > - View paint events in real-time to identify costly paint events that may be harming the performance of your animations.

4. How Browsers Work

- [How content is rendered](https://developer.mozilla.org/en-US/docs/Learn/Performance/What_is_web_performance#how_content_is_rendered)
  > - How the browser works
  > - Source order
  > - The critical path
  > - The document object model
  > - Latency
