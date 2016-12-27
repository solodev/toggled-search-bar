# search-bar-dropdown
Giving your website visitors the ability to quickly search your entire website provides a better user experience and allows website visitors to find the right content without having to go through your entire website manually searching for the content they are looking for. However, adding a search bar to every page of your website can pose design problems, search bars can take up a lot of room and interfere with the navigation or design of your website.

In this tutorial, we teach you how to add a search icon button to your website navigation that populates a search bar when clicked. This allows you to provide the ability to search your website without interfering in the design and user experience of your website. In this article, [Solodev](https://www.solodev.com/) teaches you how to add a clickable search icon to your website navigation that populates a search form onClick.

## Tutorial

For detailed instructions, view Solodev's [Creating a Dropdown Website Search Menu](https://www.solodev.com/blog/web-design/creating-a-dropdown-website-search-menu.stml) article.

## Demo

Try out a working example on [JSFiddle](https://jsfiddle.net/solodev/cdzow8z8/).

## HTML

The search bar dropdown contains the following basic HTML markup.

```
<nav class="navbar navbar-inverse navbar-fixed-top">
   <div class="container">
      <div class="navbar-header">
         <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
         <span class="sr-only">Toggle navigation</span>
         <span class="icon-bar"></span>
         <span class="icon-bar"></span>
         <span class="icon-bar"></span>
         </button>
         <a class="navbar-brand" href="#">Project name</a>
      </div>
      <div id="navbar" class="navbar-collapse collapse">
         <div class="navbar-form navbar-right">
            <a onclick="documentTrack('#search');" href="#search" class="search-form-tigger btn btn-success"  data-toggle="search-form"><i class="fa fa-search" aria-hidden="true"></i></a>
         </div>
         <!--/.navbar-collapse -->
      </div>
   </div>
</nav>
<div class="search-form-wrapper">
   <form class="search-form" id="" action="">
      <div class="input-group">
         <input type="text" name="search" class="search form-control" placeholder="Search">
         <span class="input-group-addon" id="basic-addon2"><i class="fa fa-search" aria-hidden="true"></i>
         </span>
         <span class="input-group-addon" id="basic-addon2"><i class="fa fa-window-close" aria-hidden="true"></i>
         </span>
      </div>
   </form>
</div>
<!-- Main jumbotron for a primary marketing message or call to action -->
<div class="jumbotron">
   <div class="container">
      <h1>Hello, world!</h1>
      <p>This is a template for a simple marketing or informational website. It includes a large callout called a jumbotron and three supporting pieces of content. Use it as a starting point to create something more unique.</p>
      <p><a class="btn btn-primary btn-lg" href="#" role="button">Learn more &raquo;</a></p>
   </div>
</div>
<div class="container">
   <!-- Example row of columns -->
   <div class="row">
      <div class="col-md-4">
         <h2>Heading</h2>
         <p>Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui. </p>
         <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
      </div>
      <div class="col-md-4">
         <h2>Heading</h2>
         <p>Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui. </p>
         <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
      </div>
      <div class="col-md-4">
         <h2>Heading</h2>
         <p>Donec sed odio dui. Cras justo odio, dapibus ac facilisis in, egestas eget quam. Vestibulum id ligula porta felis euismod semper. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.</p>
         <p><a class="btn btn-default" href="#" role="button">View details &raquo;</a></p>
      </div>
   </div>
   <hr>
   <footer>
      <p>&copy; 2016 Company, Inc.</p>
   </footer>
</div>
<!-- /container -->
```

## CSS

All necessary CSS is included in the file popup-search-bar.css

## JavaScript

The search bar popup uses the following basic JavaScript.

```
$( document ).ready(function() {
$('[data-toggle=search-form]').click(function() {
    $('.search-form-wrapper').toggleClass('open');
    $('.search-form-wrapper .search').focus();
    $('html').toggleClass('search-form-open');
  });
  $('[data-toggle=search-form-close]').click(function() {
    $('.search-form-wrapper').removeClass('open');
    $('html').removeClass('search-form-open');
  });
$('.search-form-wrapper .search').keypress(function( event ) {
  if($(this).val() == "Search") $(this).val("");
});

$('.search-form-wrapper').click(function(event) {
  $('.search-form-wrapper').removeClass('open');
  $('html').removeClass('search-form-open');
});
});
```
## External Includes

This tutorial contains the following third party resources.

```
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<link rel="stylesheet" href="popup-search-bar.css">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
```
