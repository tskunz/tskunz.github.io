---
layout: page
title: BeerBreweriesShiny
description: RshinyApp
img: assets/img/beer.jpg
importance: 2
category: work
related_publications: 
---

<!DOCTYPE html>

<html>

<head>

<meta charset="utf-8" />
<meta name="generator" content="pandoc" />
<meta http-equiv="X-UA-Compatible" content="IE=EDGE" />


<meta name="author" content="TK" />

<meta name="date" content="2023-11-07" />

<title>BBShiny</title>

<script src="site_libs/header-attrs-2.24/header-attrs.js"></script>
<script src="site_libs/jquery-3.6.0/jquery-3.6.0.min.js"></script>
<meta name="viewport" content="width=device-width, initial-scale=1" />
<link href="site_libs/bootstrap-3.3.5/css/bootstrap.min.css" rel="stylesheet" />
<script src="site_libs/bootstrap-3.3.5/js/bootstrap.min.js"></script>
<script src="site_libs/bootstrap-3.3.5/shim/html5shiv.min.js"></script>
<script src="site_libs/bootstrap-3.3.5/shim/respond.min.js"></script>
<style>h1 {font-size: 34px;}
       h1.title {font-size: 38px;}
       h2 {font-size: 30px;}
       h3 {font-size: 24px;}
       h4 {font-size: 18px;}
       h5 {font-size: 16px;}
       h6 {font-size: 12px;}
       code {color: inherit; background-color: rgba(0, 0, 0, 0.04);}
       pre:not([class]) { background-color: white }</style>
<script src="site_libs/navigation-1.1/tabsets.js"></script>
<link href="site_libs/highlightjs-9.12.0/default.css" rel="stylesheet" />
<script src="site_libs/highlightjs-9.12.0/highlight.js"></script>

<style type="text/css">
  code{white-space: pre-wrap;}
  span.smallcaps{font-variant: small-caps;}
  span.underline{text-decoration: underline;}
  div.column{display: inline-block; vertical-align: top; width: 50%;}
  div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
  ul.task-list{list-style: none;}
    </style>

<style type="text/css">code{white-space: pre;}</style>
<script type="text/javascript">
if (window.hljs) {
  hljs.configure({languages: []});
  hljs.initHighlightingOnLoad();
  if (document.readyState && document.readyState === "complete") {
    window.setTimeout(function() { hljs.initHighlighting(); }, 0);
  }
}
</script>









<style type = "text/css">
.main-container {
  max-width: 940px;
  margin-left: auto;
  margin-right: auto;
}
img {
  max-width:100%;
}
.tabbed-pane {
  padding-top: 12px;
}
.html-widget {
  margin-bottom: 20px;
}
button.code-folding-btn:focus {
  outline: none;
}
summary {
  display: list-item;
}
details > summary > p:only-child {
  display: inline;
}
pre code {
  padding: 0;
}
</style>


<style type="text/css">
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu>.dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
  border-radius: 0 6px 6px 6px;
}
.dropdown-submenu:hover>.dropdown-menu {
  display: block;
}
.dropdown-submenu>a:after {
  display: block;
  content: " ";
  float: right;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
  border-width: 5px 0 5px 5px;
  border-left-color: #cccccc;
  margin-top: 5px;
  margin-right: -10px;
}
.dropdown-submenu:hover>a:after {
  border-left-color: #adb5bd;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left>.dropdown-menu {
  left: -100%;
  margin-left: 10px;
  border-radius: 6px 0 6px 6px;
}
</style>

<script type="text/javascript">
// manage active state of menu based on current page
$(document).ready(function () {
  // active menu anchor
  href = window.location.pathname
  href = href.substr(href.lastIndexOf('/') + 1)
  if (href === "")
    href = "index.html";
  var menuAnchor = $('a[href="' + href + '"]');

  // mark the anchor link active (and if it's in a dropdown, also mark that active)
  var dropdown = menuAnchor.closest('li.dropdown');
  if (window.bootstrap) { // Bootstrap 4+
    menuAnchor.addClass('active');
    dropdown.find('> .dropdown-toggle').addClass('active');
  } else { // Bootstrap 3
    menuAnchor.parent().addClass('active');
    dropdown.addClass('active');
  }

  // Navbar adjustments
  var navHeight = $(".navbar").first().height() + 15;
  var style = document.createElement('style');
  var pt = "padding-top: " + navHeight + "px; ";
  var mt = "margin-top: -" + navHeight + "px; ";
  var css = "";
  // offset scroll position for anchor links (for fixed navbar)
  for (var i = 1; i <= 6; i++) {
    css += ".section h" + i + "{ " + pt + mt + "}\n";
  }
  style.innerHTML = "body {" + pt + "padding-bottom: 40px; }\n" + css;
  document.head.appendChild(style);
});
</script>

<!-- tabsets -->

<style type="text/css">
.tabset-dropdown > .nav-tabs {
  display: inline-table;
  max-height: 500px;
  min-height: 44px;
  overflow-y: auto;
  border: 1px solid #ddd;
  border-radius: 4px;
}

.tabset-dropdown > .nav-tabs > li.active:before, .tabset-dropdown > .nav-tabs.nav-tabs-open:before {
  content: "\e259";
  font-family: 'Glyphicons Halflings';
  display: inline-block;
  padding: 10px;
  border-right: 1px solid #ddd;
}

.tabset-dropdown > .nav-tabs.nav-tabs-open > li.active:before {
  content: "\e258";
  font-family: 'Glyphicons Halflings';
  border: none;
}

.tabset-dropdown > .nav-tabs > li.active {
  display: block;
}

.tabset-dropdown > .nav-tabs > li > a,
.tabset-dropdown > .nav-tabs > li > a:focus,
.tabset-dropdown > .nav-tabs > li > a:hover {
  border: none;
  display: inline-block;
  border-radius: 4px;
  background-color: transparent;
}

.tabset-dropdown > .nav-tabs.nav-tabs-open > li {
  display: block;
  float: none;
}

.tabset-dropdown > .nav-tabs > li {
  display: none;
}
</style>

<!-- code folding -->




</head>

<body>


<div class="container-fluid main-container">




<div class="navbar navbar-default  navbar-fixed-top" role="navigation">
  <div class="container">
    <div class="navbar-header">
      <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-bs-toggle="collapse" data-target="#navbar" data-bs-target="#navbar">
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
      <a class="navbar-brand" href="index.html">Trevor Website</a>
    </div>
    <div id="navbar" class="navbar-collapse collapse">
      <ul class="nav navbar-nav">
        <li>
  <a href="index.html">Home</a>
</li>
<li>
  <a href="About-Me.html">About Me</a>
</li>
<li class="dropdown">
  <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
    Case Study 1 - Beers &amp; Breweries
     
    <span class="caret"></span>
  </a>
  <ul class="dropdown-menu" role="menu">
    <li>
      <a href="Kunz_Merajmohammadi_Beers_Breweries.html">R-Markdown Project File</a>
    </li>
    <li>
      <a href="https://tkunz.shinyapps.io/BBShiny/">Interactive R Shiny Application</a>
    </li>
  </ul>
</li>
      </ul>
      <ul class="nav navbar-nav navbar-right">
        
      </ul>
    </div><!--/.nav-collapse -->
  </div><!--/.container -->
</div><!--/.navbar -->

<div id="section-header">



<h1 class="title toc-ignore">BBShiny</h1>
<h4 class="author">TK</h4>
<h4 class="date">2023-11-07</h4>

</div>


<div id="section-rshiny-test" class="section level2">
<h2>Rshiny Test</h2>
<p>This is a test of an RShiny app in RMarkdown</p>
<pre class="r"><code>library(shiny)
library(ggplot2)
beers_breweries = read.csv(&quot;https://raw.githubusercontent.com/tskunz/tskunz.github.io/main/beers_breweries.csv&quot;)

# Sort the unique states alphabetically
sorted_states &lt;- sort(unique(beers_breweries$State))
# Sort the unique styles alphabetically
sorted_styles &lt;- sort(unique(beers_breweries$Style))

ui &lt;- fluidPage(
  
  titlePanel(&quot;Beers Brewery Shiny App&quot;),
  
  sidebarLayout(
    sidebarPanel(
      sliderInput(inputId = &quot;bins&quot;,
                  label = &quot;Number of bins:&quot;,
                  min = 1,
                  max = 50,
                  value = 23),
      
      radioButtons(inputId = &quot;variable&quot;,
                   label = &quot;Select Variable:&quot;,
                   choices = c(&quot;IBU&quot;, &quot;ABV&quot;),
                   selected = &quot;IBU&quot;),
      
      # Add a filter for &quot;State&quot; with alphabetically sorted choices
      selectInput(inputId = &quot;state&quot;,
                  label = &quot;Select State:&quot;,
                  choices = c(&quot;All&quot;, sorted_states),
                  selected = &quot;All&quot;),
                  
      # Add a filter for &quot;Style&quot; with alphabetically sorted choices
      selectInput(inputId = &quot;style&quot;,
                  label = &quot;Select Style:&quot;,
                  choices = c(&quot;All&quot;, sorted_styles),
                  selected = &quot;All&quot;),
                  
      # Add a radio button for choosing the plot type
      radioButtons(inputId = &quot;plot_type&quot;,
                   label = &quot;Select Plot Type:&quot;,
                   choices = c(&quot;Histogram&quot;, &quot;Box Plot&quot;, &quot;Scatter Plot&quot;),
                   selected = &quot;Histogram&quot;),
                   
      # Add a checkbox to toggle the regression line on and off
      checkboxInput(inputId = &quot;show_regression&quot;,
                    label = &quot;Show Regression Line&quot;,
                    value = FALSE)
    ),
    
    mainPanel(
      plotOutput(outputId = &quot;plot&quot;)
    )
  )
)

server &lt;- function(input, output) {
  
  output$plot &lt;- renderPlot({
    
    filtered_data &lt;- beers_breweries
    if (input$state != &quot;All&quot;) {
      # Filter data by the selected state
      filtered_data &lt;- subset(beers_breweries, State == input$state)
    }
    
    if (input$style != &quot;All&quot;) {
      # Filter data by the selected style
      filtered_data &lt;- subset(filtered_data, Style == input$style)
    }
    
    if (input$plot_type == &quot;Histogram&quot;) {
      # Histogram
      variable_data &lt;- if (input$variable == &quot;IBU&quot;) filtered_data$IBU else filtered_data$ABV
      bins &lt;- seq(min(variable_data), max(variable_data), length.out = input$bins + 1)
      hist(variable_data, breaks = bins, col = &quot;#75AADB&quot;, border = &quot;white&quot;,
           xlab = input$variable,
           main = if (input$variable == &quot;IBU&quot;) &quot;Histogram of IBU&quot; else &quot;Histogram of ABV&quot;)
    } else if (input$plot_type == &quot;Box Plot&quot;) {
      # Box plot with black lines
      variable_data &lt;- if (input$variable == &quot;IBU&quot;) filtered_data$IBU else filtered_data$ABV
      boxplot(variable_data, col = &quot;#75AADB&quot;, border = &quot;black&quot;,
              xlab = input$variable,
              main = if (input$variable == &quot;IBU&quot;) &quot;Box Plot of IBU&quot; else &quot;Box Plot of ABV&quot;)
    } else {
      # Scatter plot
      variable_data_x &lt;- if (input$variable == &quot;IBU&quot;) filtered_data$IBU else filtered_data$ABV
      variable_data_y &lt;- if (input$variable == &quot;IBU&quot;) filtered_data$ABV else filtered_data$IBU
      plot_title &lt;- if (input$variable == &quot;IBU&quot;) &quot;Scatter Plot of IBU vs. ABV&quot; else &quot;Scatter Plot of ABV vs. IBU&quot;
      
      p &lt;- ggplot(filtered_data, aes(x = variable_data_x, y = variable_data_y)) +
        geom_point() +
        xlab(input$variable) + ylab(if (input$variable == &quot;IBU&quot;) &quot;ABV&quot; else &quot;IBU&quot;) +
        ggtitle(plot_title)
        
      if (input$show_regression) {
        p &lt;- p + geom_smooth(method = &quot;lm&quot;, se = FALSE, col = &quot;orange&quot;)
      }
      
      print(p)
    }
    
  })
  
}

shinyApp(ui, server)</code></pre>
<iframe data-deferred-src="app05242c37e6a0e5736a32a5de364bfc3a/?w=&amp;__subapp__=1" width="100%" height="400" class="shiny-frame shiny-frame-deferred"></iframe>
</div>




</div>

<script>

// add bootstrap table styles to pandoc tables
function bootstrapStylePandocTables() {
  $('tr.odd').parent('tbody').parent('table').addClass('table table-condensed');
}
$(document).ready(function () {
  bootstrapStylePandocTables();
});


</script>

<!-- tabsets -->

<script>
$(document).ready(function () {
  window.buildTabsets("section-TOC");
});

$(document).ready(function () {
  $('.tabset-dropdown > .nav-tabs > li').click(function () {
    $(this).parent().toggleClass('nav-tabs-open');
  });
});
</script>

<!-- code folding -->


<!-- dynamically load mathjax for compatibility with self-contained -->
<script>
  (function () {
    var script = document.createElement("script");
    script.type = "text/javascript";
    script.src  = "https://mathjax.rstudio.com/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML";
    document.getElementsByTagName("head")[0].appendChild(script);
  })();
</script>

</body>
</html>