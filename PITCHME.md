## Sponsors

---

Conf thanks

---

<img class="rounded" src="assets/img/me.png" height="420" />

@snap[north span-80]
@emoji[wave text-14] @css[text-14](Hi, I'm Chris DeMars)
@snapend

@snap[south-west fit]
<img src="assets/img/mvp.png" />
@snapend

@snap[south-east fit]
<img src="assets/img/gde.png" />
@snapend

@snap[south]
<img src="assets/img/work.png" />
@snapend

---

### @css[title glow](Run to the Light Carol Anne)

#### @css[title](Auditing with Lighthouse)

![Logo](assets/img/poltergeist.jpg)

---

## What is an audit?

---

@quote[Analysis of how your experience is doing.]

---

@ul

- Performance
- SEO (Search Engine Optimization)
- Best Practices
- PWA (Progressive Web App)
- Accessibility
  @ulend

---

@snap[midpoint]
<img src="assets/img/perf-ss.png" />
@snapend

---

[Webpage Test](https://www.webpagetest.org/)

---

Keywords, Structure, Description, Google Analytics, etc.

[A Simple (But Effective) 31-Point SEO Checklist](https://ahrefs.com/blog/seo-checklist/)

---

## Best Practices

#### Proper doctype, no console errors, etc.

---

## @css[title](Security & HTTPS)

@snap[south-middle span-100 fragment]
@[2, zoom-18]

```html
<div class="...">
  <a href="..." rel="noopener"></a>
</div>
```

@snapend

---

## Progressive Web Apps

---

@snap[north-east span-100 text-06]
Sample sw.js file
@snapend
@snap[span-100]

```javascript
if ('serviceWorker' in navigator) {
  window.addEventListener('load', function() {
    navigator.serviceWorker.register('/sw.js').then(
      function(registration) {
        // Registration was successful
        console.log(
          'ServiceWorker registration successful with scope: ',
          registration.scope
        );
      },
      function(err) {
        // registration failed :(
        console.log('ServiceWorker registration failed: ', err);
      }
    );
  });
}
```

@snapend

---

@snap[north-east span-100 text-06]
Sample manifest.json file
@snapend
@snap[span-100]

```javascript zoom-06
{
  "short_name": "Maps",
  "name": "Google Maps",
  "icons": [
    {
      "src": "/images/icons-192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
    {
      "src": "/images/icons-512.png",
      "type": "image/png",
      "sizes": "512x512"
    }
  ],
  "start_url": "/maps/?source=pwa",
  "background_color": "#3367D6",
  "display": "standalone",
  "scope": "/maps/",
  "theme_color": "#3367D6"
}
```

@[2-4, zoom-21]
@[6-8, zoom-21]
@[11-13, zoom-21]
@[16-20, zoom-21]

@snapend

---

@snap[north-east span-100 text-06]
Tell the browser about your manifest.json file
@snapend
@snap[span-100]

```html midpoint zoom-15
<link rel="manifest" href="/manifest.json" />
```

@snapend

---

## @css[title](Accessibility)

---

@snap[north-east span-100 text-06]
Semantic markup and ARIA
@snapend[west]

```html zoom-10
<header>
  <!--- Some code goes here --->
</header>
<section>
  <!--- Some code goes here --->
</section>
<div class="...">
  <ul>
    <li aria-label="some label"></li>
    <li aria-label="some label"></li>
    <li aria-label="some label"></li>
  </ul>
</div>
<footer>
  <!--- Some code goes here --->
</footer>
```

@[1-3, zoom-15]
@[4-6, zoom-15]
@[7-13, zoom-15]
@[14-16, zoom-15]

---

## How do we audit?

---

@snap[midpoint lighthouse]
<img src="assets/img/lighthouse.svg" />
@snapend

---

## OFF WE GO TO CHROME!

<img src="https://media.giphy.com/media/GlO8owuLggHhm/giphy.gif" width="480" height="208"/>
