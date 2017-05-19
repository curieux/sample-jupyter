
.. code:: python

    import numpy as np
    import pandas as pd
    X = np.random.randn(100,2)


.. code:: python

    import bokeh.plotting, bokeh.io
    bokeh.io.output_notebook()



.. raw:: html

    
        <div class="bk-root">
            <a href="http://bokeh.pydata.org" target="_blank" class="bk-logo bk-logo-small bk-logo-notebook"></a>
            <span id="8b3e4cc1-6f59-46ff-9d16-b2b548cd5335">Loading BokehJS ...</span>
        </div>




.. code:: python

    canvas = bokeh.plotting.figure()
    canvas.circle(X[:,0], X[:,1])
    bokeh.io.show(canvas)



.. raw:: html

    
    
        <div class="bk-root">
            <div class="bk-plotdiv" id="b5eb5c35-f807-4247-919e-8cc5b2c45b5b"></div>
        </div>
    <script type="text/javascript">
      
      (function(global) {
        function now() {
          return new Date();
        }
      
        var force = false;
      
        if (typeof (window._bokeh_onload_callbacks) === "undefined" || force === true) {
          window._bokeh_onload_callbacks = [];
          window._bokeh_is_loading = undefined;
        }
      
      
        
        if (typeof (window._bokeh_timeout) === "undefined" || force === true) {
          window._bokeh_timeout = Date.now() + 0;
          window._bokeh_failed_load = false;
        }
      
        var NB_LOAD_WARNING = {'data': {'text/html':
           "<div style='background-color: #fdd'>\n"+
           "<p>\n"+
           "BokehJS does not appear to have successfully loaded. If loading BokehJS from CDN, this \n"+
           "may be due to a slow or bad network connection. Possible fixes:\n"+
           "</p>\n"+
           "<ul>\n"+
           "<li>re-rerun `output_notebook()` to attempt to load from CDN again, or</li>\n"+
           "<li>use INLINE resources instead, as so:</li>\n"+
           "</ul>\n"+
           "<code>\n"+
           "from bokeh.resources import INLINE\n"+
           "output_notebook(resources=INLINE)\n"+
           "</code>\n"+
           "</div>"}};
      
        function display_loaded() {
          if (window.Bokeh !== undefined) {
            document.getElementById("b5eb5c35-f807-4247-919e-8cc5b2c45b5b").textContent = "BokehJS successfully loaded.";
          } else if (Date.now() < window._bokeh_timeout) {
            setTimeout(display_loaded, 100)
          }
        }
      
        function run_callbacks() {
          window._bokeh_onload_callbacks.forEach(function(callback) { callback() });
          delete window._bokeh_onload_callbacks
          console.info("Bokeh: all callbacks have finished");
        }
      
        function load_libs(js_urls, callback) {
          window._bokeh_onload_callbacks.push(callback);
          if (window._bokeh_is_loading > 0) {
            console.log("Bokeh: BokehJS is being loaded, scheduling callback at", now());
            return null;
          }
          if (js_urls == null || js_urls.length === 0) {
            run_callbacks();
            return null;
          }
          console.log("Bokeh: BokehJS not loaded, scheduling load and callback at", now());
          window._bokeh_is_loading = js_urls.length;
          for (var i = 0; i < js_urls.length; i++) {
            var url = js_urls[i];
            var s = document.createElement('script');
            s.src = url;
            s.async = false;
            s.onreadystatechange = s.onload = function() {
              window._bokeh_is_loading--;
              if (window._bokeh_is_loading === 0) {
                console.log("Bokeh: all BokehJS libraries loaded");
                run_callbacks()
              }
            };
            s.onerror = function() {
              console.warn("failed to load library " + url);
            };
            console.log("Bokeh: injecting script tag for BokehJS library: ", url);
            document.getElementsByTagName("head")[0].appendChild(s);
          }
        };var element = document.getElementById("b5eb5c35-f807-4247-919e-8cc5b2c45b5b");
        if (element == null) {
          console.log("Bokeh: ERROR: autoload.js configured with elementid 'b5eb5c35-f807-4247-919e-8cc5b2c45b5b' but no matching script tag was found. ")
          return false;
        }
      
        var js_urls = [];
      
        var inline_js = [
          function(Bokeh) {
            (function() {
              var fn = function() {
                var docs_json = {"bccce64d-f364-4caa-8791-09098007fbed":{"roots":{"references":[{"attributes":{"formatter":{"id":"2697ae62-32b0-4029-8785-2a50f6f5cb30","type":"BasicTickFormatter"},"plot":{"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"},"ticker":{"id":"4094770d-422a-4525-b4f8-81dbc7813a21","type":"BasicTicker"}},"id":"2caba980-cd85-415b-9a38-ad389f1cb5d2","type":"LinearAxis"},{"attributes":{},"id":"4094770d-422a-4525-b4f8-81dbc7813a21","type":"BasicTicker"},{"attributes":{"dimension":1,"plot":{"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"},"ticker":{"id":"4094770d-422a-4525-b4f8-81dbc7813a21","type":"BasicTicker"}},"id":"999be776-6e06-4f03-a03c-421b34ba7227","type":"Grid"},{"attributes":{"data_source":{"id":"be3b8c1e-6e81-4a5e-bf05-e081c608e1cb","type":"ColumnDataSource"},"glyph":{"id":"0db6c5cf-94cc-484e-8be4-7eaf488e45e8","type":"Circle"},"hover_glyph":null,"nonselection_glyph":{"id":"3967eb44-f1a2-4cf3-91b1-25b5c4a123b9","type":"Circle"},"selection_glyph":null},"id":"2dec38b1-d2f9-45ea-8bac-84f789df355a","type":"GlyphRenderer"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"value":"#1f77b4"},"line_alpha":{"value":0.1},"line_color":{"value":"#1f77b4"},"x":{"field":"x"},"y":{"field":"y"}},"id":"3967eb44-f1a2-4cf3-91b1-25b5c4a123b9","type":"Circle"},{"attributes":{"bottom_units":"screen","fill_alpha":{"value":0.5},"fill_color":{"value":"lightgrey"},"left_units":"screen","level":"overlay","line_alpha":{"value":1.0},"line_color":{"value":"black"},"line_dash":[4,4],"line_width":{"value":2},"plot":null,"render_mode":"css","right_units":"screen","top_units":"screen"},"id":"b667c0b8-34bb-4c09-b4f7-66504b5fb5f9","type":"BoxAnnotation"},{"attributes":{"plot":{"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"}},"id":"c62a310a-2f7c-405d-865d-1f900603cd42","type":"PanTool"},{"attributes":{"fill_color":{"value":"#1f77b4"},"line_color":{"value":"#1f77b4"},"x":{"field":"x"},"y":{"field":"y"}},"id":"0db6c5cf-94cc-484e-8be4-7eaf488e45e8","type":"Circle"},{"attributes":{},"id":"ab3f2c23-8910-4765-bcf9-50d81886b43c","type":"BasicTickFormatter"},{"attributes":{"plot":{"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"}},"id":"f3e3342b-0e28-414e-86e4-a1ba58c52b5c","type":"WheelZoomTool"},{"attributes":{"overlay":{"id":"b667c0b8-34bb-4c09-b4f7-66504b5fb5f9","type":"BoxAnnotation"},"plot":{"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"}},"id":"e3243e5f-424c-40e7-ae59-90f8ca4d9c87","type":"BoxZoomTool"},{"attributes":{"plot":{"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"}},"id":"aa26cc50-9b94-4c43-84a2-1cba16de70cd","type":"SaveTool"},{"attributes":{"plot":{"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"}},"id":"92ce4a38-a625-4a5d-96ce-55e407d4db54","type":"ResetTool"},{"attributes":{"plot":{"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"}},"id":"09cdb885-bb7a-4535-bec1-f9187b5e5173","type":"HelpTool"},{"attributes":{},"id":"2697ae62-32b0-4029-8785-2a50f6f5cb30","type":"BasicTickFormatter"},{"attributes":{"callback":null,"column_names":["x","y"],"data":{"x":{"__ndarray__":"jEG4jAb47z+OM5RsMJsAQGd7v1/JV+u/HBOBGDqd4z+pE71oF1gKwE5KaAduS9O/0QqWKxl63b8RXI88Q5Dsv0+hkYeW9O6/9FUU7FEHvj+9NemuMPriP9KcYxk/wuI/9Hv00ZdY6T8w9XVLUK7iP0ge4q4Uot0/Venp09zJzr/a+9dDm7nov03IUQgxDP2/s5gvfxR45r9/2VQkabX7Py5n+tnxsvG/yLJdUcRM6T/vgqtu+wgEwAcisYlQN9m/N8rh0NSp8b/v/3sMmc/fPzkf+yrYnbg/IKLuCmxu8j8DPCXMgrjAP8LefOP8QL0/wONkqxFDyr+7JzBb0EPkvyO3xx3x9Nw/H31d/N/b3T9VBCXm4RP5P8+nGObFX9g/TgFOISLVAcDEdgcNkz3sP2Az7cC4GIW/+cLba6Tr1r+4ZIDAJfTQP1BtEyFyCZC/38FXwe939j9iAEG+agTxP/r8MIJQpv6/2V4AMVjN57+stYdja4vmP7dYf9veUKY/LR0bmo+Yy798w/+6WB8HwL/u3oGwROS/TYmPmc6//j/cjkmOOuDNvxzVKQIOEOg/G13D+Xj/zD+p4s9SlaLRP0yU3X1JQ9E/OsVTXVJo4b/0OjK+LQKvP/jGOmGxNfo/tm8a++Hh9D95JpfHIr70v7zGwkpzxLK/FJwD4Eev079VHNe32YzaP2k0KjfcONY/f5DPt3Kdxz/Fa8xKTSj2P0TJmHK/H8M/eMhxiiWnwr9uVB94mbTzv+vWhH01QvS/bJaCA3PI2L/T5Fm011b2P0nNjUccy9Q/Erqftr4ivD9UlBUekg+3v3sDg/9y++g/Gut9M54QmD+wzdmZJs7WP+QzsCQob7o/p0I19mdD6T+3e7oqI1axP+UgPRwCvNw/xdPl4fys5b+x10b7rWHsvzwVKZZHb/C/K7/Nv1GKwr8jMD9baOnqPwcw1Vg6Naq/RWmSBG4nA0DPlg/1G3fvP6a8WZDfPbu//iTvV+nf6T++SB78ABasP8clKH6jwcY/rnUJC3Sw9r8TxDqv6C5Kv/Ad3/K0ccO/OFhHefJo5L8=","dtype":"float64","shape":[100]},"y":{"__ndarray__":"zi5hEXAG7L8vKdehCBv7vxz7PZIo9ZO/AscvxA8qjj/dvt0rXL4DwHVb28zaO/O/LVDvt+ZC7L+eDdMjSrwCQG50wc/6XOQ/f6ERBgIg3L+LC5WNbq+6vz7Xq5UE4Oy/0E+9sCGt3z9Rs74Bl83vP/faLFHo+ty/si3HAOuH7L/1Uq9s3ATaP0TnA6MQzfg/nwUSUsLh1T8kDvbNCjMDwK48rfQ7n+W/dDnVUDDJvL+lJ/VPmFTgP/E79H7I+cu/VjHbidFE6r9OoXpv10nUP29ULjyp3uK/KHL03sch4j833PsK2inYPweC4lwu67g/pa6vxlTLyD+zGP7EZG7hP9b8EXqr/t2/9ER2xSWKs7/dO7yRwOnyP1Yqg/nWjPa/UKAm+sab9j8XW6hXxMLcP7FKJ+ihnNS/D+q7WHHT8T8z+1Eye3X7P4QB7PzVRNu/EgHrZ3GO4D8jhLzjPT/xv80s58hZF4C/4Ohr70tN97/DRrM3RAbCvyKVmXopFOw/HNOwJKg8zT8Ip3oOUwzRP5pieM7VUt6/0bb0FynD9j/eLcUsXVn8v+bSsejXLve/PGA7mvtWyr8w6dMdYbLZP3byntHzBdm/ZJep/a4cAEA0SBYULnv4P1bMfYO6cNE/+/4EZ9179r/tSfaShwLgPw/A0FmwOuS/yCfMwW5L0z8TKWRadNfNP00hTLlCrNQ/rMnNv526AsCYYfELwDD0vxmd94n1mMo/klnWeC7l5z8qIJYhDfrNPzHJoWeX6wDAxFdjJ2sE9L8uab2ssrfivxxq16YQffg/rtnKJ4tY6L8gS/tjVYrfv4pTEvh7O/G/vuiQ57wS8r+R3+T5y4epPwSxT+GnA+0/3BQ27XgY8b/70sJ8ZSfyv3o5Q1rHwwBA1SQMrlvH879r+03qCUTmP6WzcZwuuOY/6RDKoreO8z++UFp0z7bkPyh6d1r/VO2/PL0fqnDY9b9NzbfygtbZv9MuucHFf80/TF5VMszD4z8008KqCErQP5J7OmIUP9m/oNjoNenG6T/P3/Yn6r34v2Xg4KCfFbe/msR6SDYu0T8=","dtype":"float64","shape":[100]}}},"id":"be3b8c1e-6e81-4a5e-bf05-e081c608e1cb","type":"ColumnDataSource"},{"attributes":{"below":[{"id":"6c82acc7-872f-4ff3-9031-914e822d81c2","type":"LinearAxis"}],"left":[{"id":"2caba980-cd85-415b-9a38-ad389f1cb5d2","type":"LinearAxis"}],"renderers":[{"id":"6c82acc7-872f-4ff3-9031-914e822d81c2","type":"LinearAxis"},{"id":"ca6ed69c-f7b5-457a-86e3-ecec535eed5b","type":"Grid"},{"id":"2caba980-cd85-415b-9a38-ad389f1cb5d2","type":"LinearAxis"},{"id":"999be776-6e06-4f03-a03c-421b34ba7227","type":"Grid"},{"id":"b667c0b8-34bb-4c09-b4f7-66504b5fb5f9","type":"BoxAnnotation"},{"id":"2dec38b1-d2f9-45ea-8bac-84f789df355a","type":"GlyphRenderer"}],"title":{"id":"439cc3d4-302c-4959-82ed-207479e5e86d","type":"Title"},"tool_events":{"id":"b4d54f46-2e1d-40a1-b214-66c992cc2712","type":"ToolEvents"},"toolbar":{"id":"68cd732f-96be-440f-8dd3-76282faafc04","type":"Toolbar"},"x_range":{"id":"86324768-37a7-4e5f-9c18-9485fab40e69","type":"DataRange1d"},"y_range":{"id":"4aab6c4f-9878-40ec-b738-c1f15391bed5","type":"DataRange1d"}},"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"},{"attributes":{"plot":null,"text":""},"id":"439cc3d4-302c-4959-82ed-207479e5e86d","type":"Title"},{"attributes":{},"id":"b4d54f46-2e1d-40a1-b214-66c992cc2712","type":"ToolEvents"},{"attributes":{"callback":null},"id":"86324768-37a7-4e5f-9c18-9485fab40e69","type":"DataRange1d"},{"attributes":{"active_drag":"auto","active_scroll":"auto","active_tap":"auto","tools":[{"id":"c62a310a-2f7c-405d-865d-1f900603cd42","type":"PanTool"},{"id":"f3e3342b-0e28-414e-86e4-a1ba58c52b5c","type":"WheelZoomTool"},{"id":"e3243e5f-424c-40e7-ae59-90f8ca4d9c87","type":"BoxZoomTool"},{"id":"aa26cc50-9b94-4c43-84a2-1cba16de70cd","type":"SaveTool"},{"id":"92ce4a38-a625-4a5d-96ce-55e407d4db54","type":"ResetTool"},{"id":"09cdb885-bb7a-4535-bec1-f9187b5e5173","type":"HelpTool"}]},"id":"68cd732f-96be-440f-8dd3-76282faafc04","type":"Toolbar"},{"attributes":{"callback":null},"id":"4aab6c4f-9878-40ec-b738-c1f15391bed5","type":"DataRange1d"},{"attributes":{"formatter":{"id":"ab3f2c23-8910-4765-bcf9-50d81886b43c","type":"BasicTickFormatter"},"plot":{"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"},"ticker":{"id":"acc66942-3dfb-456b-b2a6-95d03eb1f515","type":"BasicTicker"}},"id":"6c82acc7-872f-4ff3-9031-914e822d81c2","type":"LinearAxis"},{"attributes":{},"id":"acc66942-3dfb-456b-b2a6-95d03eb1f515","type":"BasicTicker"},{"attributes":{"plot":{"id":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d","subtype":"Figure","type":"Plot"},"ticker":{"id":"acc66942-3dfb-456b-b2a6-95d03eb1f515","type":"BasicTicker"}},"id":"ca6ed69c-f7b5-457a-86e3-ecec535eed5b","type":"Grid"}],"root_ids":["7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d"]},"title":"Bokeh Application","version":"0.12.4"}};
                var render_items = [{"docid":"bccce64d-f364-4caa-8791-09098007fbed","elementid":"b5eb5c35-f807-4247-919e-8cc5b2c45b5b","modelid":"7193bdbc-9a84-4f4b-b015-ba4f0ef2cc6d"}];
                
                Bokeh.embed.embed_items(docs_json, render_items);
              };
              if (document.readyState != "loading") fn();
              else document.addEventListener("DOMContentLoaded", fn);
            })();
          },
          function(Bokeh) {
          }
        ];
      
        function run_inline_js() {
          
          if ((window.Bokeh !== undefined) || (force === true)) {
            for (var i = 0; i < inline_js.length; i++) {
              inline_js[i](window.Bokeh);
            }if (force === true) {
              display_loaded();
            }} else if (Date.now() < window._bokeh_timeout) {
            setTimeout(run_inline_js, 100);
          } else if (!window._bokeh_failed_load) {
            console.log("Bokeh: BokehJS failed to load within specified timeout.");
            window._bokeh_failed_load = true;
          } else if (force !== true) {
            var cell = $(document.getElementById("b5eb5c35-f807-4247-919e-8cc5b2c45b5b")).parents('.cell').data().cell;
            cell.output_area.append_execute_result(NB_LOAD_WARNING)
          }
      
        }
      
        if (window._bokeh_is_loading === 0) {
          console.log("Bokeh: BokehJS loaded, going straight to plotting");
          run_inline_js();
        } else {
          load_libs(js_urls, function() {
            console.log("Bokeh: BokehJS plotting callback run at", now());
            run_inline_js();
          });
        }
      }(this));
    </script>


