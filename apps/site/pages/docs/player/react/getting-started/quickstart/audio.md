---
layout: quickstart
title: Audio Player Installation
description: Instructions to get your audio player installed and on-screen using React.
---

{% step %}

### Install NPM Package {% slot="title" %}

{% slot name="description" %}
Install `@vidstack/player-react` and dependencies via NPM.
{% /slot %}

```bash {% copy=true %}
npm i lit @vidstack/player@next @vidstack/player-react@next
```

{% /step %}

{% step %}

### Import Components {% slot="title" %}

{% slot name="description" %}
Import media components into the `jsx` or `tsx` file where you'll be building your player.
{% /slot %}

```js {% copy=true %}
import { Audio, Media } from '@vidstack/player-react';
```

{% /step %}

{% step %}

### Add Player Markup {% slot="title" %}

{% slot name="description" %}
Add the following player JSX boilerplate to get started.
{% /slot %}

```jsx {% copy=true %}
<Media>
  <Audio>
    <audio src="https://media-files.vidstack.io/audio.mp3" preload="none" />
  </Audio>
</Media>
```

{% /step %}

{% step %}

### Hydrate (SSR) {% slot="title" %}

{% slot name="description" %}
Import the hydration module in the root application (i.e., `_app.jsx`) _or_ page
component containing your player.
{% /slot %}

```jsx {% copyHighlight=true highlight="3" %}
// Only required if pre-rendering or SSR.
// E.g., Next.js or Remix.
import '@vidstack/player/hydrate.js';
```

{% /step %}
