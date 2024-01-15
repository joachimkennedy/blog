---
title: "Posts"
date: 2022-12-29T10:48:59-08:00
---

{{ range first 5 .Pages }}
  <article>
  <div>
    <h2><a href="{{ .RelPermalink }}">{{ .Title }}</a></h2>
    {{ .Summary }}
  </div>
  </article>
{{ end }}

