---
layout:     post
title:      "Thoughts about working style"
date:       2017-03-24 15:48:00+0800
categories: [thoughts]
tags:       [stuff,thoughts]
---
### 短期目标与长期目标

以Best Practice的方式做一个User Story，假设需要10个mhr。

以Work Around的方式先做一个prototype、或者为了某个可demo的目标，假设需要3个mhr。

但是，从这样一个短期的实现，到最终的完成，并没有足够的重用性，也就是，之后还需要10个mhr。

如果把重用性考虑进去，那么短期的目标需要8个mhr，之后继续做需要3个mhr。

可能真实情况下，单就一个User Story，两者差的不多，从长期看，孰优孰劣，一目了然，好比O(log(n))和O(n)

<table class="table table-bordered table-striped table-condensed">
  <tr>
    <th>index</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
    <th>mhr</th>
  </tr>
  <tr>
    <td>1</td>
    <td colspan="10" align="center">Best Practice</td>
  </tr>
  <tr>
    <td>2</td>
    <td colspan="3" align="center">Work Around</td>
    <td colspan="10" align="center">Rest</td>
  </tr>
  <tr>
    <td>3</td>
    <td colspan="8" align="center">Demo</td>
    <td colspan="3" align="center">Rest</td>
  </tr>
</table>
