---
title: Dark Theme
description: Change the color scheme of your application.
docs: 'theming/dark-theme.md'
---

<script>
  import { Demo, ThemeDemos } from '@svelteuidev/demos';
  import { Heading } from 'components';

  const styles = `<style id='svelteui-inject-body' type='text/css'>.article>*:nth-child(3){margin-top:15rem!important;}@media(max-width: 800px){.article>*:nth-child(3){margin-top:18rem!important;}}<\/style>`;
</script>

<svelte:head>
{@html styles}
</svelte:head>

<Heading />

## Getting Started

Without any additional steps, all SvelteUI components support the dark color scheme by default. Wrap your application in SvelteUIProvider and specify the `themeObserver` prop to use a dark color scheme:

<Demo demo={ThemeDemos.darkTheme} />

## Global styles

`theme.colors["dark700"].value` shade is considered to be the body background color and `theme.colors["dark50"].value` shade is used as text color with dark color scheme. You can add them by setting the `withGlobalStyles` prop on SvelteUIProvider, which includes them by default:

```svelte
<script>
	import { SvelteUIProvider } from '@svelteuidev/core';
</script>

<SvelteUIProvider withGlobalStyles themeObserver={'dark'}>
	<YourApp />
</SvelteUIProvider>
```

## More to come

We are in constant development, so here are some things you can expect down the line:

- Subscribe to theme changes throughout the app
- Saving theme in local storage
- Changing theme based on keyboard shortcut
- Detect preferred color scheme
