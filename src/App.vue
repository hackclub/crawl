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

    <h2>requirements</h2>

    <p>
      Spend two or more hours coding your own web crawler, get $10 to buy a video game (or multiple) of your choice from Steam or Itch.io!
    </p>

    <p>
      Your web crawler needs to be able to look at HTML and output itsy bitsy data points, it's that simple! Choose any website you like, and try to get something from it. You could extract the links from a Wikipedia page and do something with them, or even make a web crawler that moves between pages!
    </p>

    <p>
      Any questions? Join <a href="https://hackclub.enterprise.slack.com/archives/C0C7N079Z2Q">#crawl</a> and <a href="https://hackclub.enterprise.slack.com/archives/C0C8CLLC6DN">#crawl-help</a> on the Slack!
    </p>

    <p>
      <a href="" class="cta">submit your project</a>
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
body {
  background: #14100b;
  color: #f2e8d5;
  /* Lora for body copy: real 400-700 range, so font-weight:bold is a true
     bold. Shadows Into Light is single-weight and only legible at display
     sizes, so it's reserved for the h1 below. */
  font-family: "Lora", serif;
  margin: 0;
  /* the corner webs and spider can poke past the viewport on narrow
     screens; clip them so there's no sideways scrollbar */
  overflow-x: hidden;
}
.page {
  max-width: 560px;
  margin: 60px auto;
  padding: 0 16px;
}
:root {
  /* base size of web1 (512px source); web2 is the same art at 1024px,
     so it renders at 2x this to appear identically sized */
  --web-size: 240px;
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
@media (max-width: 600px) {
  :root {
    --web-size: 150px;
  }
}
.title {
  position: relative;
  display: inline-block;
}
h1 {
  font-family: "Shadows Into Light", cursive;
  font-size: 64px;
  letter-spacing: 8px;
  margin: 0;
  color: #ff8c1a;
}

h2 {
  font-family: "Shadows Into Light", cursive;
  line-height: 1.2;
}

.spider {
  position: absolute;
  top: -34px;
  left: 100%;
  margin-left: -8px;
  width: var(--spider-size);
  height: auto;
  pointer-events: none;
  user-select: none;
  -webkit-user-select: none;
  -webkit-touch-callout: none;
  -webkit-user-drag: none;
}
.tag {
  font-weight: bold;
}
hr {
  border: none;
  border-top: 1px dashed #ff8c1a;
  margin: 24px 0;
}
.cta {
  display: inline-block;
  color: #14100b;
  background: #ff8c1a;
  padding: 8px 16px;
  text-decoration: none;
  font-weight: bold;
}

.cta:hover,
.cta:focus-visible {
  text-decoration: none;
  outline: dashed #ff8c1a;
  outline-offset: 2px;
}

footer {
  font-size: 14px;
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  justify-content: space-between;
  background-color: #361b03;
  padding: 8px 12px;
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
  gap: 12px;
}
</style>
