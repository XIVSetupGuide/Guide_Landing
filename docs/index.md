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
      src: /images/home-page-start.png
      height: 100%
      width: 100%
    link: "https://start.xivsetup.guide/"
    title: "FFXIV Install Guide"
    details: "A complete guide to installing Final Fantasy XIV, from platform selection to installing."
  - icon:
      src: /images/home-page-wiiu.jpg
      height: 100%
      width: 100%
    link: "https://wiiu.hacks.guide/"
    title: "Wii U Hacks Guide"
    details: "A guide collaboration between Nintendo Homebrew's Helpers and Staff, from stock to Aroma custom firmware."
  - icon:
      src: /images/home-page-vita.jpg
      height: 100%
      width: 100%
    link: "https://vita.hacks.guide/"
    title: "Vita Hacks Guide"
    details: "A complete guide to PS Vita (TV) custom firmware, from stock to Ensō."
  - icon:
      src: /images/home-page-wii.jpg
      height: 100%
      width: 100%
    link: "https://wii.hacks.guide/"
    title: "Wii Hacks Guide"
    details: "The complete guide to modding your Wii, vWii, and Wii mini."
  - icon:
      src: /images/home-page-switch.png
      height: 100%
      width: 100%
    link: "https://switch.hacks.guide/"
    title: "Switch Hacks Guide"
    details: "A complete guide to Switch custom firmware, from stock to Atmosphere."
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
