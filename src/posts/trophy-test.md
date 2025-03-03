---
title: Trophy Test
description: A test of the trophy component.
date: '2025-3-3'
categories:
  - sveltekit
  - svelte
published: true
---

<script>
  import TrophyCard from '$lib/components/TrophyCard/TrophyCard.svelte';
</script>



## Trophy Card

The counter is rendered inside Markdown.

<TrophyCard 
  rarity="platinum"
  name="Test"
  desc="Test Trophy Description"
/>