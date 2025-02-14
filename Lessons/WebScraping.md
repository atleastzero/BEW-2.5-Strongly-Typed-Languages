# 📜 Day 6: Scraping the Web

### ⏱ Lesson Plan

1. [[**05m**] 🏆 Objectives](#05m--objectives)
2. [[**05m**] 🤷‍♀️ Why You Should Know This](#05m-️-why-you-should-know-this)
3. [[**15m**] 📖 Overview: Web Scraping](#15m--overview-web-scraping)
4. [[**20m**] 💻 Game: Selector Diner](#20m--game-selector-diner)
5. [[**10m**] 💻 Demo: Selecting Selectors](#10m--demo-selecting-selectors)
6. [[**10m**] BREAK](#10m-break)
7. [[**15m**] 📖 Overview: Colly](#15m--overview-colly)
8. [[**30m**] 💻 Activity: Work Out a Workflow](#30m--activity-work-out-a-workflow)
9. [[**55m**] 🧪 Lab Time: Begin Web Scraper Project](#55m--lab-time-begin-web-scraper-project)
10. [📚 Resources & Credits](#-resources--credits)

## [**05m**] 🏆 Objectives

1. Identify the critical steps to collecting data using web scraping techniques.
2. Apply selectors to an HTML document to retreive data.
3. Design and create a web scraper that retrieves data from your favorite website!

## [**05m**] 🤷‍♀️ Why You Should Know This

- All projects need data before launching!
- Available datasets may not meet your needs or require additional supporting data from a source on the web.
- Save important data before a website goes offline for archival purposes.

## [**15m**] 📖 Overview: Web Scraping

Web Scrapers crawl a website, extract it's data, transform that data to a usable structured format, finally writing it to a file or database for subsequent use.

<p align="center">
  <img src="https://www.scrapehero.com/wp/wp-content/uploads/2018/01/xhow-does-a-web-scraper-work-simple-2.png.pagespeed.ic.MeNRriGmi9.webp">
</p>

Programs that use this design pattern follow the **Extract-Transform-Load (ETL) Process**.

### Web Crawling vs. Web Scraping

- Not interchangeable terms!
- Crawlers download and store the contents of large numbers of sites by following the links in pages.
    - How Google got famous
- Scrapers are built for the structure of a specific website.
    - Use site's own structure to extract individual specific data elements.
    - Crawling is the first step to web scraping.

### Parsing & Extracting Data Using Selectors

Below are the most common selectors used when scraping the web for the purposes of data collection.

| Name                 | Syntax          | Description                                                  |
| -------------------- | --------------- | ------------------------------------------------------------ |
| **Element**          | `a`             | Any element  `section`, `a`, `table`, etc.                   |
| **ID**               | `#home-link`    | First element with `id="video-player"`                       |
| **Class**            | `.blog-post`    | Any element with `class="blog-post"`                         |
| **Attribute**        | `a[href]`       | All values of the `href` attribute assigned to any `a` element |
| **Pseudo-Attribute** | `a:first-child` | The first `a` element                                        |

Let's practice selectors now --- they're the most important part of writing an awesome web scraper! If the selector isn't correct, nothing will return, and no data will have been collected as a result of running your scraper.

## [**20m**] 💻 Game: Selector Diner

Choose the right plates while working the window at the [CSS Diner](https://flukeout.github.io/). This fun game will level up your selector skills in preparation for your Web Scraper project.

## [**10m**] 💻 Demo: Selecting Selectors

_Instructor will demonstrate how to find and test selectors in Chrome before integrating them in your web scraper._

### Techniques Demonstrated

- Inspect an element > right click it's node in the DOM tree > choosing Copy > Copy Selector.
- Testing using `Ctrl` + `F` in the inspector.

**If your selector does not work using these methods, it WILL NOT WORK IN YOUR SCRAPER**!

## [**10m**] BREAK

## [**15m**] 📖 Overview: Colly

A popular open source package, [Colly](https://go-colly.org), provides a clean foundation to write any kind of crawler/scraper/spider. Features include:

- Lots of cool Go language concepts!
- Fast (>1k request/sec on a single core)
- Manages request delays and maximum concurrency per domain
- Automatic cookie and session handling
- Sync/async/parallel scraping
- Distributed scraping
- Caching

### Starter Code

Starter code is included in the [project repository](https://github.com/make-school-labs/makescraper). Let's go through it together!

### Callbacks

Colly works via a series of callbacks that are executed anytime `Visit()` is called on a collector.

Callbacks are functions that execute after another function completes.

Colly supports the following callbacks:

```golang
c.OnRequest(func(r *colly.Request) {
    fmt.Println("Visiting", r.URL)
})

c.OnError(func(_ *colly.Response, err error) {
    log.Println("Something went wrong:", err)
})

c.OnResponse(func(r *colly.Response) {
    fmt.Println("Visited", r.Request.URL)
})

c.OnHTML("a[href]", func(e *colly.HTMLElement) {
    e.Request.Visit(e.Attr("href"))
})

c.OnHTML("tr td:nth-of-type(1)", func(e *colly.HTMLElement) {
    fmt.Println("First column of a table row:", e.Text)
})

c.OnXML("//h1", func(e *colly.XMLElement) {
    fmt.Println(e.Text)
})

c.OnScraped(func(r *colly.Response) {
    fmt.Println("Finished", r.Request.URL)
})
```

With a partner, use the sample code to determine which order these callbacks fire in. Paste the above snippet, build, and run `./makescraper` to see the output.

### More Examples

- [**Colly**: Docs](http://go-colly.org/docs/): Check out the sidebar for 20+ examples!
- [**Ali Shalabi**: Syntax-Helper](https://github.com/alishalabi/syntax-helper): Command line interface to help generate proper code syntax, pulled from the Golang documentation.

## [**30m**] 💻 Activity: Work Out a Workflow

_Complete the workflow worksheet distributed in class._

When you're done, use the remaining lab time to begin your project!

## [**55m**] 🧪 Lab Time: Begin Web Scraper Project

Read the project [README](https://github.com/make-school-labs/makescraper) to begin your project.

You'll be able to complete at least a few requirements after what you've learned today.

We'll learn how to serialize and store JSON during our next class!

## 📚 Resources & Credits

- [**ScrapeHero**: What is Web Scraping – Part 1 – Beginner’s Guide](https://www.scrapehero.com/a-beginners-guide-to-web-scraping-part-1-the-basics/)
- [**W3C**: Selectors](https://www.w3.org/TR/CSS22/selector.html)
- [Colly](https://go-colly.org): Starter code derived from [basic](http://go-colly.org/docs/examples/basic/) example.
