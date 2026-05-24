---
layout: about
title: Home
permalink: /

selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---



<div class="conference-bg" markdown="1">

Wearable and ubiquitous computing has facilitated the widespread aggregation and analysis of health data for individuals. The growing availability of health information enables the use of artificial intelligence to process, interpret, and act on the data. While companies and researchers continue to explore new hardware options for wearables like watches, rings, necklaces, and even footwear research, there will be more opportunities to explore how AI can be embedded into wearable hardware.

In this Ubicomp '26 workshop, we aim to reframe the conversation around ”Physical AI” beyond robotics to include wearable devices that can aggregate, analyze, and act on users' physiological health data. Our health is integral in how we interact with the physical world and devices designed to capture biomarkers and other signals used in inferring a person’s health are becoming more and more common. Additional biomarkers, usability, diagnosis accuracy, privacy, etc are all topics that will become increasingly important as more individuals rely on these devices to track their personal health.

We propose this workshop as a way to discuss the current landscape, how AI will influence research, and challenges we see ahead. There have been no recent review papers describing building of health wearable devices and Ubicomp will be a good venue to bring the research community together for a more updated group discussion. This is especially important as this space changes very quickly with new sensors and AI architectures coming out yearly.

</div>

<style>
.conference-bg {
  position: relative;
  padding: 3rem;
  border-radius: 24px;
  overflow: hidden;
  background:
    linear-gradient(rgba(10, 20, 35, 0.68), rgba(10, 20, 35, 0.68)),
    url('/assets/img/wearable_health.png') center center / cover no-repeat;
  color: white;
  min-height: 60vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  box-shadow: 0 18px 40px rgba(0, 0, 0, 0.18);
}

.conference-bg p {
  max-width: 900px;
  font-size: 1.08rem;
  line-height: 1.9;
  color: white;
}

@media (max-width: 768px) {
  .conference-bg {
    padding: 1.5rem;
    min-height: auto;
    border-radius: 18px;
  }

  .conference-bg p {
    font-size: 1rem;
    line-height: 1.75;
  }
}
</style>