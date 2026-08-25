---
layout: home
title: "XIVSetup.Guide"
hero:
  text: "XIVSetup.Guide"
  tagline: "Complete guides to setting up Final Fantasy XIV, the launcher, plugins, and more!"
  image:
    src: /images/home-page-feature.jpg
features:
  - icon:
      src: /images/home-page-start.jpg
      height: 100%
      width: 100%
    link: "https://start.xivsetup.guide/"
    title: "FFXIV Install Guide"
    details: "A complete guide to installing Final Fantasy XIV, from platform selection to installing."
  - icon:
      src: /images/home-page-xivlauncher.jpg
      height: 100%
      width: 100%
    link: "https://xivlauncher.xivsetup.guide/"
    title: "XIVLauncher Guide"
    details: "Guidance on how to install/setup/configure the third party launcher, XIVLauncher."
  - icon:
      src: /images/home-page-penumbra.jpg
      height: 100%
      width: 100%
    link: "https://penumbra.xivsetup.guide/"
    title: "Modding/Plugins Guide"
    details: "Setting up your Modding Plugins/Tools/etc for FFXIV"
  - icon:
      src: /images/home-page-lightless.jpg
      height: 100%
      width: 100%
    link: "https://lightless.xivsetup.guide/"
    title: "Installing/Configuring Lightless Sync"
    details: "Installing and setting up Lightless Sync so you can see other people's mods"
  - icon:
      src: /images/home-page-mods.jpg
      height: 100%
      width: 100%
    link: "https://mods.xivsetup.guide/"
    title: "Finding/Installing Mods"
    details: "How to find/install/configure mods"
  - icon:
      src: /images/home-page-plugins.jpg
      height: 100%
      width: 100%
    link: "https://plugins.xivsetup.guide/"
    title: "Finding/Installing Plugins"
    details: "How to find/install/configure plugins"
---

<script setup>
import { ref } from 'vue'

const showPopup = ref(true)
</script>

<Teleport to="body">
  <div
    v-if="showPopup"
    class="guide-popup-overlay"
    @click.self="showPopup = false"
  >
    <div class="guide-popup">
      <button
        class="guide-popup-close"
        @click="showPopup = false"
        aria-label="Close"
      >×</button>
      <h2>Welcome to the site! Please select what you're here for (or close the window to select manually)</h2>
      <p>Choose an option below to get started</p>
      <div class="guide-popup-options">
        <a href="https://start.xivsetup.guide/" class="guide-popup-option">I know nothing about XIV and want to install/set it up</a>
        <a href="https://xivlauncher.xivsetup.guide/" class="guide-popup-option">I have XIV installed but am using the original launcher</a>
        <a href="https://penumbra.xivsetup.guide/" class="guide-popup-option">I'm already using XIVLauncher and want to set up modding plugins</a>
        <a href="https://lightless.xivsetup.guide/" class="guide-popup-option">I already set up the modding plugins and I want to set up Lightless (the sync plugin)</a>
        <a href="https://mods.xivsetup.guide/" class="guide-popup-option">I'm interested in finding mods</a>
        <a href="https://plugins.xivsetup.guide/" class="guide-popup-option">I'm interested in other recommended plugins</a>
      </div>
    </div>
  </div>
</Teleport>
