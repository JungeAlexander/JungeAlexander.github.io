---
layout: post
title: test

---

This is a test:


This is an RNA container.

<div id='rna_ss'> </div>

This after the RNA container.

<script src="//d3js.org/d3.v3.min.js" charset="utf-8"></script>
<script src="//code.jquery.com/jquery-1.12.0.min.js"></script>
<script src='{{BASE_PATH}}/assets/scripts/fornac.js'></script>

<script type='text/javascript'>
var container = new fornac.FornaContainer("#rna_ss",
        {'applyForce': true, 'allowPanningAndZooming': true, 'initialSize':[500,300]});

var options = {'structure': '..((..((...[)).(((..].))).))..',
    'sequence': 'AACGCUUCAUAUAAUCCUAAUGACCUAUAA'
};
/*
var options1 = {'structure': '.((((....)))).',
    'sequence': 'GCGGCGAUUGCCGG'
};
*/

var options1 = {'structure': '..............',
    'sequence': 'GCGGCGAUUGCCGG'
};

//container.changeColorScheme('custom')
/*
   var options = {'structure': '((...)).',
   'sequence':             'CCCCCCCC'
   };
 */

//container.transitionRNA(options1.structure);
container.addRNA(options.structure, options);
container.setSize();

</script>
