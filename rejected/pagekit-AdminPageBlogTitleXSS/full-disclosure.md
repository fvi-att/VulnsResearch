# Title
Pagekit AdminPage Blog Title has Stored XSS.

I post same full disclosure into [here](https://github.com/pagekit/pagekit/issues/894)

## Summery

When Authenticated attacker post crafted the blog post. Any kind of Javascript is executed on browsers of users who access to crafted blog post page.

## Reproduction

Here is how to reproduct this issue.
See issuepage.


## Payloads

```html
test<script>alert(0);</script>
```

## Response

This issue is tought as not vulnerable.
```
Pagekits posts and pages provide HTML support as a feature (like Wordpress, Joomla and many other CMSs), which implies that code injection is always possible for users with write permissions. I won't consider this a problem since write permissions should only be granted to trusted parties (users with write permissions can cause a lot of harm anyway, even besides code injection).
```

## Event

- 2018-03-08 Vuln is discoverd. 
- 2018-03-09 post issue on [github](https://github.com/pagekit/pagekit/issues/894)
- 2018-03-11 post return that this is not vuln.
- 2018-03-12 close this issue.

