### Selection
+ d3.select
+ d3.selectAll
+ ```classed('class')``` returns whether or not selected elements contain ```class```. Chaining unavailable.
+ ```d3.selectAll('.house').classed('frog', true)``` gives a class ```frog``` to all satisfying ```div```s, false also available. Chaining also available here.1

### D3 Requests
+ d3.json
```javascript
  d3.json('phones.json', function(err, data) {
    console.log(err);
    console.log(data);
  });
```
+ d3.csv
```javascript
  d3.csv('phones.json', function(err, data) {
    ///
  });
```

### SVG
```javascript
  function createSVG() {
    mySVG = d3.select('body').append('svg')
                                .attr('height', '800')
                                .attr('width', '500');
    mySVG.append('circle')
            .attr('id', 'start')
            .attr('class', 'foobar');
    mySVG.append('circle')
            .attr('id', 'end')
            .attr('class', 'foobar');
    mySVG.append('line')
            .attr('class', 'foobar');
  }
```
### Data Binding
```javascript
  dots = viz.selectAll('cirlce')
              .data(data)
              .enter()
              .append('circle');
  dots.attr('r', function(d) { return Math.abs(d.TMAX); });
```