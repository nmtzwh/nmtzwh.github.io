---
layout: post
title: "Backup Atom from one computer to another"
date: 2016-06-22
---

Copy all the `*.cson, *.json, *.less, *.coffee` in `~/.atom` directory.

	apm list --install --bare > packages.list (old computer)
	apm install `cat packages.list` (new computer)
