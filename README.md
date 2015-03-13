# bezier-forward-diff
Bezier subdivision via forward differencing

## install

`npm install bezier-forward-diff`

## use
    var bezier = require('./bezier');
    var zeroes = require('zeroes');

    var newInput = [ [ 0, 0, 0 ],
                     [ 0, 0, 1 ],
                     [ 0, 1, 1 ],
                     [ 1, 1, 1 ] ];

    var segments = 7;

    // preallocate the result array
    var result = zeroes( [ segments + 1, 3 ] ); // n + 1 points define n segments

    bezier(result, newInput, segments);

    console.log(result);

## thanks

Forward Difference Calculation of Bezier Curves
By Curtis Bartley, November 01, 1997

http://www.drdobbs.com/forward-difference-calculation-of-bezier/184403417?pgno=5

## license

MIT