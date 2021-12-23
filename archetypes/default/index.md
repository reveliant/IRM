---
title: {{ replaceRE "^[0-9]+-" "" .Name | title }}
weight: {{ replaceRE "^([0-9]+)-.*" "$1" .Name }}
description: 
author: CERT SG / 
version: 1.
---
