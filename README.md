# Legacy Shred Snap policy entrypoint

`index.html` redirects to `https://shredsnap.app/privacy-policy/` using
`location.replace`. An explicit `?lang=ja` / `?lang=en` takes precedence over
`#ja` / `#en`; otherwise the destination chooses the browser language. Unrelated
queries and fragments are not forwarded. A noscript meta refresh and direct
Japanese/English links provide fallbacks. This is a static HTML redirect, not
an HTTP 301/308.

Only the root/index entrypoint moves. `icon.png` and all `mockImages/` assets
remain served at their existing paths (the app still references them).

[The new-site PR](https://github.com/Sidebook/shred-snap-static-sites/pull/1)
was merged on October 19, 2026. Its Pages deployment succeeded and the updated
policy is available. This redirect can be published after review.
