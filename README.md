# Backbone Lawnchair Adapter

A drop-in implementation of `Backbone.sync` that uses a Lawnchair instance for client-side persistence.

[Lawnchair](http://westcoastlogic.com/lawnchair/) is a simple JSON storage engine that implements several legacy techniques for persistence. If you're using a modern browser that implements the DOM `localStorage` APIs, you should probably use [backbone.localStorage](https://github.com/jeromegn/Backbone.localStorage) instead.

## Usage

Include `backbone.lawnchair.js` after `backbone.js`:

    <script type="text/javascript" src="backbone.js"></script>
    <script type="text/javascript" src="backbone.lawnchair.js"></script>

Then specify the Lawnchair instance to use for each collections like so:

    window.SomeCollection = Backbone.Collection.extend({
      
      lawnchair: = new Lawnchair({ name: "SomeCollection"}, new Function()), // Unique name within your app.
      
      // ... everything else is normal.
      
    });
  
## Credits

Based on [backbone.localStorage](https://github.com/jeromegn/Backbone.localStorage) by Jerome Gravel-Niquet and others.

