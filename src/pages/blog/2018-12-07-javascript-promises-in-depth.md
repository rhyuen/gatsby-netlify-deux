---
templateKey: blog-post
title: Javascript Promises in Depth
date: 2018-12-08T02:04:54.797Z
description: >-
  Promises are used as an abstraction for Asynchronous programming in
  Javascript.
tags:
  - async promise json api edd
---
A `Promise` is a placeholder for the pending response of an asynchronous call, like `axios.get()` or `fetch(url)`.  

There are three states of a `Promise`: "Pending", "Fulfilled" and "Rejected".

When using `fetch`, it is often the case where after calling `fetch(url)` that a `.then(res => res.json()).then(data => {...})` block of code is written.  This is due to the face that the `Promise` returned by `fetch(url)` returns a `Promise` and that returned `Promise` has a method `.json()` that also returns a `Promise`, hence the need for two `.then()` methods after calling `fetch(url)` before anything can be done with the data.
