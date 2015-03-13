# bezier-forward-diff
Bezier subdivision via forward differencing

###example###
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