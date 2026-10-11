<script setup>
import webCornerLeft from './assets/web1.webp'
import webCornerRight from './assets/web2.webp'
import spiderArt from './assets/spider.webp'
</script>

<template>
  <main class="page">
    <img
      class="corner-web corner-web--left"
      :src="webCornerLeft"
      alt=""
      draggable="false"
    />
    <img
      class="corner-web corner-web--right"
      :src="webCornerRight"
      alt=""
      draggable="false"
    />

    <div class="title">
      <h1>Crawl</h1>
      <img class="spider" :src="spiderArt" alt="" draggable="false" />
    </div>
    <p class="tag">Build your own web crawler, get a video game!</p>

    <hr />

    <p>Take just <strong>2 or more hours</strong> coding your very own web crawler and get <strong>$10</strong> to spend on a video game (or several) from Steam or Itch.io!</p> If you chose to spend <strong>6 hours</strong> on your crawler, we'll give you the choice between <strong>Minecraft</strong> or a <strong>$30 video game grant</strong>!
    
    <h2>requirements</h2>
    
    <ul>
      <li>It looks at a page's HTML and extracts itsy bitsy data points. That's it!</li>
      <li>Any website works, so pick your favorite</li>
      <li>It (obviously) adheres to <a href="https://hackclub.com/conduct">Hack Club's CoC</a></li>
    </ul>

    <h2>ideas</h2>

    <ul>
      <li>Grab every link on a Wikipedia article and do something fun with them</li>
      <li>Make a crawler that traverses the internet autonomously by following links</li>
    </ul>

    <p>
      Coding time is calculated with <a href="https://hackatime.hackclub.com/">Hackatime!</a> Check it out, and set it up before starting!
    </p>

    <p>
      Any questions? Join <a href="https://hackclub.enterprise.slack.com/archives/C0C7N079Z2Q">#crawl</a> and <a href="https://hackclub.enterprise.slack.com/archives/C0C8CLLC6DN">#crawl-help</a> on the Slack!
    </p>

    <h3>FYI: the YSWS is no longer accepting submissions. Thank you to any participants!</h3>

    <p>
      <a href="https://forms.hackclub.com/t/pqMvL6JyMHus" class="cta">submit your project</a>
    </p>

    <hr />

    <footer>
      <div class="left-side">
        <a href="https://hackclub.com">Hack Club</a>
        <a href="https://hackclub.com/privacy-and-terms">Terms & Privacy Policy</a>
      </div>
      <div class="right-side">
        <a href="https://forms.hackclub.com/bounty">Fulfillment bounty</a>
        <a href="https://security.hackclub.com/">Security</a>
      </div>
    </footer>
  </main>
</template>

<style>
html {
    font-family: "Shadows Into Light Two", cursive;
  /* everything below is in rem, so this one value scales the whole page:
     16px on phones, growing with viewport width up to 20px on big monitors */
  font-size: clamp(16px, 0.35vw + 12px, 20px);
  /* the corner webs and spider can poke past the viewport on narrow
     screens; clip them so there's no sideways scroll. Set on html too
     because mobile Safari ignores overflow on body alone */
  overflow-x: clip;
}
body {
  background: #14100b;
  color: #f2e8d5;
  /* Lora for body copy: real 400-700 range, so font-weight:bold is a true
     bold. Shadows Into Light is single-weight and only legible at display
     sizes, so it's reserved for the h1 below. */
  font-family: "Lora", serif;
  margin: 0;
  overflow-x: clip;
}
.page {
  max-width: 35rem;
  margin: 3.75rem auto;
  padding: 0 1rem;
}
:root {
  /* base size of web1 (512px source); web2 is the same art at 1024px,
     so it renders at 2x this to appear identically sized */
  --web-size: clamp(7rem, 14vw, 16rem);
  /* spider is a 256px source. Equal drawing scale with the 512px web1 would
     be 0.5; trimmed to 0.52 so the spider reads as a smaller accent. Change
     this one number to resize it and it stays tied to --web-size. */
  --spider-size: calc(var(--web-size) * 0.52);
}
.corner-web {
  position: absolute;
  top: 0;
  height: auto;
  pointer-events: none;
  user-select: none;
  -webkit-user-select: none;
  -webkit-touch-callout: none;
  -webkit-user-drag: none;
}
.corner-web--left {
  left: 0;
  width: var(--web-size);
}
.corner-web--right {
  right: 0;
  width: calc(var(--web-size) * 2);
}
.title {
  position: relative;
  display: inline-block;
}
h1 {
  font-family: "Shadows Into Light Two", cursive;
  font-size: 3.5rem;
  letter-spacing: 0.125em;
  margin: 0;
  color: #ff8c1a;
}

h2 {
  font-family: "Shadows Into Light Two", cursive;
  line-height: 1.2;
}

.spider {
  position: absolute;
  top: calc(var(--spider-size) * -0.27);
  left: 100%;
  margin-left: -0.5rem;
  width: var(--spider-size);
  height: auto;
  pointer-events: none;
  user-select: none;
  -webkit-user-select: none;
  -webkit-touch-callout: none;
  -webkit-user-drag: none;
}
li::marker {
  color: #ff8c1a;
}
.tag {
  font-weight: bold;
}
hr {
  border: none;
  border-top: 1px dashed #ff8c1a;
  margin: 1.5rem 0;
}
.cta {
  display: inline-block;
  color: #14100b;
  background: #ff8c1a;
  padding: 0.5rem 1rem;
  text-decoration: none;
  
}

.cta:hover,
.cta:focus-visible {
  text-decoration: none;
  outline: dashed #ff8c1a;
  outline-offset: 0.125rem;
}

footer {
  font-size: 0.875rem;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  justify-content: space-between;
  background-color: #361b03;
  padding: 0.5rem 0.75rem;
}

a {
  color: #ff8c1a;
}

a:hover {
  text-decoration: underline wavy;
}

footer div {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
}
</style>
