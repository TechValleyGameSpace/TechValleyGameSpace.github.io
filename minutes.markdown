---
layout: page
title: Board Meeting Minutes
permalink: /minutes/
---

As we migrate over to this new site layout we're working on making all our past meeting minutes availible.
Please feel free to reach out if you're looking for minutes that are not listed below.

<html>
  <body>
    <script>
      (async () => {
        const response = await fetch('https://api.github.com/repos/TechValleyGameSpace/TechValleyGameSpace.github.io/contents/files/board_minutes/');
        const data = await response.json();
        let htmlString = '<ul>';
        
        for (let file of data) {
          htmlString += `<li><a href="${file.path}">${file.name}</a></li>`;
        }

        htmlString += '</ul>';
        document.getElementsByTagName('body')[0].innerHTML = htmlString;
      })()
    </script>
  <body>
</html>
