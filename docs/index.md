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
      src: /images/home-page-3ds.jpg
      height: 100%
      width: 100%
    link: "https://3ds.hacks.guide/"
    title: "3DS Hacks Guide"
    details: "A complete guide to 3DS (and 2DS) custom firmware, from stock to boot9strap."
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
  - icon:
      src: /images/home-page-test.png
      height: 100%
      width: 100%
    link: "https://start.xivsetup.guide/"
    title: "FFXIV Install Guide"
    details: "Proof of Concept test guide used to learn how stuff works here"
---

---

<script setup>
import { ref } from 'vue'

const showPopup = ref(true)
</script>

<Teleport to="body">
  <Transition name="guide-popup">
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
        >
          ×
        </button>

        <h2>Welcome to the site! Please select what you're here for (or close the window to select manually)</h2>
        <p>Choose an option below to get started</p>

        <div class="guide-popup-options">
          <a href="start.xivsetup.guide" class="guide-popup-option">
            I know nothing about XIV and want to install/set it up
          </a>

          <a href="xivlauncher.xivsetup.guide" class="guide-popup-option">
            I have XIV installed but am using the original launcher
          </a>

          <a href="penumbra.xivsetup.guide" class="guide-popup-option">
            I'm already using XIVLauncher and want to set up modding plugins
          </a>

          <a href="lightless.xivsetup.guide" class="guide-popup-option">
            I already set up the modding plugins and I want to set up Lightless (the sync plugin)
          </a>

          <a href="mods.xivsetup.guide" class="guide-popup-option">
            I'm interested in finding mods
          </a>
          
          <a href="plugins.xivsetup.guide" class="guide-popup-option">
            I'm interested in other recommended plugins
          </a>
        </div>
      </div>
    </div>
  </Transition>
</Teleport>

<style>
.guide-popup-overlay {
  position: fixed;
  inset: 0;
  z-index: 9999;

  display: flex;
  align-items: center;
  justify-content: center;

  padding: 20px;

  background: rgba(0, 0, 0, 0.7);
  backdrop-filter: blur(5px);
}

.guide-popup {
  position: relative;

  width: 100%;
  max-width: 600px;

  padding: 32px;

  border: 1px solid var(--vp-c-divider);
  border-radius: 16px;

  background: var(--vp-c-bg);
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.4);

  text-align: center;
}

.guide-popup h2 {
  margin: 0 0 8px;
  border: 0;
}

.guide-popup p {
  margin: 0 0 24px;
  color: var(--vp-c-text-2);
}

.guide-popup-close {
  position: absolute;
  top: 10px;
  right: 14px;

  border: 0;
  background: none;

  color: var(--vp-c-text-2);
  font-size: 28px;
  line-height: 1;

  cursor: pointer;
}

.guide-popup-close:hover {
  color: var(--vp-c-text-1);
}

.guide-popup-options {
  display: grid;
  gap: 12px;
}

.guide-popup-option {
  display: block;

  padding: 14px 20px;

  border: 1px solid var(--vp-c-brand-1);
  border-radius: 10px;

  background: var(--vp-c-brand-1);
  color: var(--vp-c-white) !important;

  font-weight: 600;
  text-decoration: none !important;

  transition:
    background-color 0.2s,
    transform 0.2s;
}

.guide-popup-option:hover {
  background: var(--vp-c-brand-2);
  transform: translateY(-2px);
}

/* Popup opening/closing animation */
.guide-popup-enter-active,
.guide-popup-leave-active {
  transition: opacity 0.2s ease;
}

.guide-popup-enter-active .guide-popup,
.guide-popup-leave-active .guide-popup {
  transition: transform 0.2s ease;
}

.guide-popup-enter-from,
.guide-popup-leave-to {
  opacity: 0;
}

.guide-popup-enter-from .guide-popup,
.guide-popup-leave-to .guide-popup {
  transform: scale(0.95);
}
</style>
