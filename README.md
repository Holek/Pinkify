Pinkify
=======

![Oh, Pinkie](http://images3.wikia.nocookie.net/__cb20110930130423/halo/images/f/f6/Pinkie_Pie_4th_Wall.png)

A jQuery plugin to add simple animations with sound on any event.

Getting started
---------------
You need to have an image you want to use, and know its dimensions:

    $('body').pinkify({
      'imageUrl'    : 'http://railslove.com/assets/pinkie_parasprite_polka_by_fluttershylover.gif',
      'imageWidth'  : 106,
      'imageHeight' : 126,
    });

Firing on events
----------------

Since this plugin works on all elements, oyu need to fire it up manually after a desired action, for example, after a user clicked on an element:

    $('a').bind('click', function(){
      $(this).pinkify({
       // your options passed on
      });
    });

Available options
-----------------

      var settings = $.extend( {
        'animation'   : {
          'direction' : 'left',
          'duration'  : 0.2
        },
        'imageUrl'    : 'pinkie_parasprite_polka_by_fluttershylover.gif',
        'imageWidth'  : 106,
        'imageHeight' : 126,
        'audioAttr'   : {
          // 'autoplay' : 'autoplay',
          // 'loop'     : 'true'
        },
        'aAttr'       : {
          'href'   : 'http://www.youtube.com/watch?v=6UXGEbaP5Ug&list=PL7BFEA256F3B8B0DF&index=5',
          'target' : '_blank'
        },
        'audioFiles'  : [
          // 'http://dl.dropbox.com/u/23165202/Pinkies%20Parasprite%20Polka%20%5BKeep-Mp3.com%5D.ogg',
          // 'http://dl.dropbox.com/u/23165202/Pinkies%20Parasprite%20Polka%20%5BKeep-Mp3.com%5D.mp3'
        ],
        'click' : function () {
          $(this).pinkify('destroy');
        }