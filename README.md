Auto Fetching for TV Shows
==========================

### Install

Clone and run from repo directory.

```
cp torFetchTV /usr/local/bin/torFetchTV; chmod +x /usr/local/bin/torFetchTV

```

### Usage

```
torFetchTV /path/to/show_list.json /path/to/output/
```

By default the a history file is saved to /tmp/torFetchTVhist.log to prevent multiple torrents being put into output directory. Change this by the following, the file must exists on disk before running.


```
torFetchTV /path/to/show_list.json /path/to/output/ /path/to/history.log
```



### Requirements

Nothing but php-cli 5.4+


### Sample Show List
```
[{
	"seriesMagnetLinks": "https://eztv.it/shows/525/revenge/", // web path to a page with magnet links
	"seriesPath": "dump", // local path to series, to check for existing episodes
	"scanDays": ["All"], // days to scan on [Mon, Tue, Wed, Thu, Fri, Sat, Sun, All]
	"exclude": ["720p"], // strings to exclude from results (case insensitive)
	"include": [], // strings to include from results (case insensitive)
	"timezone": "America/Los_Angeles" // show air timezone for scan days, http://php.net/manual/en/timezones.php
},{
	"seriesMagnetLinks": "https://eztv.it/shows/92/family-guy/",
	"seriesPath": "dump",
	"scanDays": ["All"],
	"exclude": ["720p"],
	"include": [],
	"timezone": "America/Los_Angeles"
}]
```
