# de-poop-twitter

> remove 💩from your Twitter timeline with a custom stylesheet.

Twitter under Mr. Poop face is adding a bunch of features which are not designed for good.

These are designed for you to :
- spend more time on the platform stuck scrolling
- get more stuck in a feedback bubble
- feel more anxious about how a tweet is performing

Safari allows users to configure a custom stylesheet:

![](https://storage.googleapis.com/shared-files-mrhenry/romain/inventive-galapagos-tortoise-0d3177f2bb.31.02.png)

```css
/* Hide "More Tweets" */
:has(head > link[rel=preconnect][href="//t.co"]) [data-testid="cellInnerDiv"]:has(h2+div) {
	display: none !important;
}

/* Hide "More Tweets" */
:has(head > link[rel=preconnect][href="//t.co"]) [data-testid="cellInnerDiv"]:has(h2+div) ~ * {
	display: none !important;
}

/* Hide "Trending" */
:has(head > link[rel=preconnect][href="//t.co"]) section:has(> [aria-label="Timeline: Trending now"]) {
	display: none !important;
}

/* Hide "Impression counter" */
:has(head > link[rel=preconnect][href="//t.co"]) [data-testid="tweet"] div:has(> a[href$="/analytics"]) {
	display: none !important;
}
```
