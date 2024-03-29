# Web Performance Metrics

## [User-centric performance metrics](https://web.dev/articles/user-centric-performance-metrics)

```mermaid
mindmap
    root(User-centric performance metrics)
        Defining metrics
            [Key questions]
                ("Is it happening?")
                ("Is it useful?")
                ("Is it usable?")
                ("Is it delightful?")
        How metrics are measured
            (In the lab)
            (In the field)
        Types of metrics
            (Perceived load speed)
            (Load responsiveness)
            (Runtime responsiveness)
            (Visual stability)
            (Smothness)
        Important metrics to measure
            ("Largest Contentful Paint (LCP)")
            ("Cumulative Layout Shift (CLS)")
            ("Interaction to Next Paint (INP)")
            ("Time to First Byte (TTFB)")
            ("First Contentful Paint (FCP)")
            ("Total Blocking Time (TBT)")
        Custom metrics
            (User Timing API)
            (Long Tasks API)
            (Element Timing API)
            (Navigation Timing API)
            (Resource Timing API)
            (Server timing)
```

### [Defining metrics](https://web.dev/articles/user-centric-performance-metrics#defining_metrics)

Key questions to ask:

<table>
    <tbody>
        <tr>
            <th>Is it happening?</th>
            <td>Did the navigation start successfully? Has the server responded?</td>
        </tr>
        <tr>
            <th>Is it useful?</th>
            <td>Has the page content rendered that the users can engage in?</td>
        </tr>
        <tr>
            <th>Is it usable?</th>
            <td>Can users interact with the page, or is it busy?</td>
        </tr>
        <tr>
            <th>Is it happening?</th>
            <td>Are the interactions smooth and natural, free of lag and jank?</td>
        </tr>
    </tbody>
</table>

### [How metrics are measured](https://web.dev/articles/user-centric-performance-metrics#how_metrics_are_measured)

* **In the lab**: using tools to simulate a page load in a consistent, controlled environment
    * Essential when developing new features
    * Used before features are released in production, when gathering real performance data is not possible
    * Best way to prevent performance regressions
* **In the field**: on real users actually loading and interacting with the page
    * Not necessarily reflective of user experiences in the wild
    * Varies dramatically based on network conditions and user interactions
    * Page loading may not be deterministic; performance may be vastly different from user to user

### [Types of metrics](https://web.dev/articles/user-centric-performance-metrics#types_of_metrics)

| Type | Description |
| --- | --- |
| Perceived load speed | how quickly a page can load and render all of its visual elements to the screen. |
| Load responsiveness | how quickly a page can load and execute any required JavaScript code in order for components to respond quickly to user interaction. |
| Runtime responsiveness | after page load, how quickly can the page respond to user interaction. |
| Visual stability | do elements on the page shift in ways that users don't expect and potentially interfere with their interactions? |
| Smoothness | Do transitions and animations render at a consistent frame rate and flow fluidly from one state to the next? |

**Note:** _No single metric_ is sufficient to capture all the performance characteristics of a page.

### [Important metrics to measure](https://web.dev/articles/user-centric-performance-metrics#important_metrics_to_measure)

| Metric | Description |
| --- | --- |
| First Contentful Paint (FCP) | measures the time from when the page starts loading to when any part of the page's content is rendered on the screen. |
| Largest Contentful Paint (LCP) | measures the time from when the page starts loading to when the largest text block or image element is rendered on the screen. |
| Interaction to Next Paint (INP) | measures the latency of every tap, click, or keyboard interaction made with the page, and—based on the number of interactions—selects the worst interaction latency of the page (or close to the highest) as a single, representative value to describe a page's overall responsiveness. |
| Total Blocking Time (TBT) | measures the total amount of time between FCP and TTI where the main thread was blocked for long enough to prevent input responsiveness. |
| Cumulative Layout Shift (CLS) | measures the time from when the page starts loading to when the largest text block or image element is rendered on the screen. |
| Time to First Byte (TTFB) | Measures the time it takes for the network to respond to a user request with the first byte of a resource. |

Read more about how to optimize these metrics in [Optimizing Metrics](./Optimizing%20Metrics.md).

## References

* [**web.dev**](https://web.dev/)
    * [Metrics](https://web.dev/explore/metrics)
    * [User-Centric Performance Metrics](https://web.dev/articles/user-centric-performance-metrics)