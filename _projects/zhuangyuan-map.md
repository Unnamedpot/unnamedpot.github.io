---
layout: project-page
title: "明清状元籍贯分布地图"
date: 2026-07-19
desc: "基于 Leaflet 与高德瓦片，可视化明清两朝 200 余位状元的籍贯地理分布，支持按朝代筛选与气泡聚类。"
landing_url: "/projects/zhuangyuan-map.html"
github_url: "https://github.com/Unnamedpot/zhuangyuan_plot"
cover: "/assets/img/projects/zhuangyuan-map/cover.png"
---

一张交互式历史地图，展示明朝（89 位）与清朝（114 位）状元的籍贯分布。数据来源于维基百科《明朝状元列表》《清朝状元列表》，地图底图使用高德地图瓦片，并对经纬度做了 WGS-84 → GCJ-02 火星坐标转换以对齐国内底图。

功能特性：

- 按朝代筛选（全部 / 明朝 / 清朝）
- 邻近籍贯(附郭县、地名更改)自动聚类，气泡大小反映人数
- 点击气泡查看该地状元名录（含年份、姓名、府县）

> 另有一张明清进士（全量 53000+）分布地图，支持省 → 府 → 县多级下钻，[点此查看](/project/jinshi-map/)。

[打开地图](/projects/zhuangyuan-map.html)