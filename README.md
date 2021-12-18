# Frontend-Interview-Cheatsheet
🔥 Frontend Interview Cheatsheet That Helped Me Get Offers From companies like Amazon &amp; LinkedIn

### Intro
Of course, there is not enough space to fit all the frontend knowledge into one article. And this is not what this cheatsheet wants to achieve. This is just a shortcut of frontend topic, that each sr frontend engineer has to be familiar with. They are frequently raised in interviews and helped me to get an offer on Amazon and LinkedIn. Enjoy reading, and feel free to dive deeper by clicking on the topic link 🙌

### Web Knowledge

#### 1. Caching

[Cache-Control](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control): instruction of request and response cache;
[Etag](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/ETag): <cache_id>check if the resource was updated by comparing <cache_id>, if not — update the cached version;

#### 2. [HTTP/2](https://www.sitepoint.com/http2-the-pros-the-cons-and-what-you-need-to-know/)

##### Pros:

- Multiple HTTP connection calls (HTTP/1 supports only 6);
- A server can push an event to a client;
- Compress headers;
- More secure

##### Cons:

- Server push can be abused;
- Can be slower if LB (Load Balancer) supports HTTP/1 and server HTTP/2

#### 3. Security

- [Transfer-Encoding](https://www.geeksforgeeks.org/http-headers-transfer-encoding/) — defines how to encrypt body: chunked, gzip;
- [Access-Control-Allow-Origin](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Origin) (Cross-Origin Resource Sharing — CORS) Defines a list of domains that can access the API of the origin domain;
- [JSONP](https://www.w3schools.com/js/js_json_jsonp.asp#:~:text=JSONP%20stands%20for%20JSON%20with,instead%20of%20the%20XMLHttpRequest%20object.) — run script to access cross-domain data (old browser);
- [X-Frame-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options) — Prevent clickjacking from iframe;
Cross-Site Request Forgery (CSRF). Attack: user has a session (logged in), attacker creates link, user clicks on the link and performs the request, attacker steals user session. Prevent: captcha, log out from visited site;
- [Content-Security-Policy](https://owasp.org/www-community/attacks/csrf) — prevent from execution harmful code;
- [X-XSS-Protection](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-XSS-Protection) — Enable XSS protection for old sites;
- [Feature-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy) — Disable not needed Browser features;
- [Referrer-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy) — when there is a link to another website from your site, by clicking it will send the URL of origin which can contain some sensitive data (user id, session);
- Don't allow the user to input any HTML innerHtml ;
- Use UI frameworks, keep node_modules updated, and limit of usage 3rd party services;

### Web Performance

#### 1. [Critical Rendering Path](https://developer.mozilla.org/en-US/docs/Web/Performance/Critical_rendering_path)

- DOM — browser compiles the Document Object Model;
- CSSOM — browser compiles the CSS Object Model;
- Render Tree — browser combines DOM and CSSOM to render the tree;
- Layout — browser computes the size and position of each of the objects;
- Paint — browser converts the tree into the pixels in the screen

Optimize CRP:
- Optimize the order of sources — load critical resources as soon as possible;
- Minimize the number of sources — reduce the number, load async;

#### 2. [Reflow](https://developers.google.com/speed/docs/insights/browser-reflow) Browser recalculates the position and geometries of the elements after rerender.

Optimize Reflow:
- reduce DOM depths;
- avoid long CSS selectors, minimize rules;

#### 3. preload, preconnect, prefetch, prerender

- [preload](https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/preload) — loads high prior sources that need to be loaded `faster<link rel="preload">;`
- [preconnect](https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/preconnect) — If some resources are required to accelerate handshake, use `<link rel="preconnect">` to reduce latency;
- [prefetch](https://developer.mozilla.org/en-US/docs/Glossary/Prefetch) — loads low prior resources and cache `<link rel="prefetch">;`
- [dns-prefetch](https://developer.mozilla.org/en-US/docs/Web/Performance/dns-prefetch) —reduce latency of resolving domain names before resources get requested `<link rel="dns-prefetch">`;
- [prerender](https://developer.mozilla.org/en-US/docs/Glossary/prerender) — similar to prefetch + caches whole the page `<link rel="prerender">`;

#### 4. Rendering Performance

**JS**

- Move the heavy task to the [web worker](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers);
- Use _[requestAnimatinFrame ](https://developer.mozilla.org/en-US/docs/Web/API/window/requestAnimationFrame)_ instead of _setTimeoutto_ perform animation;

**Style**

- reduce the complexity of selectors;
- Reduce the number of elements on which style calculation must be applied;

**Layout** (how an element is positioned and sized)

- Avoid layout changes;
- Use [flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/);
- Use [css-grid](https://itnext.io/how-i-learned-css-grid-in-5-min-ec6439d8bf0);

**Paint** (draw pixels: color, shadows; layout changes trigger repaint)

- Use [will-change](https://developer.mozilla.org/en-US/docs/Web/CSS/will-change) to optimize layout repaint;

#### 5. Workers

- Service Worker — interceptor to build an offline app;
- Web Worker — perform heavy tasks on background;

#### 6. Image Optimization

#### 7. Image optimization

**Format:**

- if animation — use <video>instead gif
- if high details and resolution — PNG
- if geometry shapes — SVG
- if text logo — use font text
- if photo — JPEG

**Compression:**

- SVG — use optimizer (like SVGO), use gzip;
- WebP — use optimized image format for Web;
- Remove metadata attributes from SVG tag;
- Use Sprites;

**Cache and Lazy Load:**

  - Use CDN for distributing static dataLazy Load images and videos 
  — Use <img loading="lazy"/> or libraries like lazysizes;

#### **DOM**
  
1. Elements
2. Manipulation
3. Document Fragment
4. Event delegation and bubbling

#### **HTML**
  
1. Semantic Elements
2. Accessibility
3. Responsive web
Javascript
1.this
2. Closure
3. Inheritance
4. Asynchronous Javascript
5. Hoisting
6. Currying
7. Higher-order functions

#### Design patterns

1. Mixin
2. Factory
3. Singleton
4. Facade
5. MVC, MVVM
6. Server vs Client-Side Rendering
  
Conclusion
  
You are Awesome ❤️
  
Learn More - https://itnext.io/frontend-interview-cheatsheet-that-helped-me-to-get-offer-on-amazon-and-linkedin-cba9584e33c7
