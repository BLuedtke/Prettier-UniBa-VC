# Prettier-UniBa-VC
Stylus Style sheet for a better (opinionated) Uni Bamberg VC appearance

## How to use
Install the Stylus extension https://addons.mozilla.org/en-US/firefox/addon/styl-us/. Add a new style for URL `vc.uni-bamberg.de`. Paste text from desired style file into the style code.

### stylus_vc_compactentries
In VC courses with lots of files in a bullet-point style list, the spacing is wasting a lot of whitespace. This makes file entries appear more compact by reducing the icon height for entries, be it files, questionnaires, etc. I heavily recommend using this!
```
.activity-item {
  padding: 0.2rem !important;
}
.section .activity {
  padding: .05rem 0;
}
.activityiconcontainer {
    max-height: 1.75rem;
}
```

### stylus_vc_compact_1 
More compact favorites in the dashboard:
```
.dashboard-card-deck:not(.fixed-width-cards) .dashboard-card {
    width: calc(15.00% - 0.5rem);
}
```

More compact images in the dashboard cards:
```
.dashboard-card-deck .dashboard-card .dashboard-card-img {
    height: 3rem;
}
```

Size-limited main content box, because default is very wide on big monitors. Adjust to your liking by changing the second and third max-width values. In my experience, the third should be smaller than the second.
```
.pagelayout-standard #page.drawers .main-inner,
body.limitedwidth #page.drawers .main-inner {
    max-width: 95%;
    max-width: 1500px;
}
#region-main-box {
    max-width: 1400px;
}
```

In "my courses", the list view is made (vertically) more compact by reducing the height of the images for each entry, and by reducing the padding.
```
.dashboard-list-img {
    height: 3rem;
}
.list-group-item {
    padding-top: 0.5rem;
    padding-bottom: 0.5rem;
}
```

Reduces the padding of the boxes on the right fold-out panel, 
as well as "add new ..." in edit mode
```
.p-3 {
    padding: 0.5rem !important;
}
```

### stylus_vc_teachersaspects
This collects a few optimizations most likely to occur to people that administer/edit VC courses.

Slightly reduces the top and bottom margins of the "Hidden" tag ("Für Teilnehmer/innen verborgen")
```
.mt-1, .my-1 {
  margin-top: 0.05rem !important;
  margin-bottom: 0.05rem !important;
}
```

In editing view, some elements have additional text telling what type of element they are. For example, above a file, it says "FILE" (or "DATEI"). This reduces the size of that text a bit:
```
.media-body .small {
    font-size: .6rem;
}
```

Tested on Firefox.