# viewportUnitPatch
Dirty jquery hack to use viewport units on any browser that can run jquery. This should include IE6+.

Viewport units are a godsend to front end devs. However, they are not fully supported across the spectrum of end user browsers. I'm trying to find a way to make that happen. 

The result is this library.

## Usage
Use a conditional tag to only load the scripts on older versions of IE
```
<!--[if lte IE 8]>
<script src="/js/jQuery-1.x.x.js"></script>
<script src="/js/vuPatch.js"></script>
<script>
$.vuPatch($(window).height(), $(window).width());
</script>
<![endif]-->
```
Then, structure elements that you want to scale to viewport units (vh or vw in CSS3) with the data types of `data-vh=` and `data-vw=`.

## Disclaimer

I know that this is not very performant in it's current state. 

This project started as a "Can I actually do that?", turned into "Wow this is possible but incredibly poorly implemented" and has now turned into "I bet I can make this useful and performant".

Watch this repo if you're interested in checking my progress in making this library production ready, or if you've got ideas on how to improve it, submit a pull request.