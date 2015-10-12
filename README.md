# Online video-downloader

Node.js & Angular.js based online video downloader. This application helps you to download videos from -




Used youtube-dl npm package :

## Getting video information :
```javascript
var youtubedl = require('youtube-dl');
var url = 'Video Link';

youtubedl.getInfo(url, function(err, info) {
  if (err) throw err;

  console.log('id:', info.id);
  console.log('title:', info.title);
  console.log('url:', info.url);
  console.log('thumbnail:', info.thumbnail);
  console.log('description:', info.description);
  console.log('filename:', info._filename);
  console.log('format id:', info.format_id);
});
```


## Downloading videos :
```javascript
  var filename = "Video URL Link";
  var fs = require('fs');
  fs.readFile(filename, function (err, data){
    if (err) return console.log(err);
    // Header setup for download
    res.writeHead(206,{
      "Content-type" : "video/mp4",
      "Content-length" : data.length,
      "Content-disposition" : "attachment; filename="+req.query.filename+".mp4"
    })

    res.send(data)
  });

```




