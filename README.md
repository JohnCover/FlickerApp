**CECS 475  
Lab Assignment 7  
Assigned date: 4/13  
Due date: 4/20**  

**10 points**

Create a Flickr Viewer app that allows users to search for photos on the photo-sharing website Flickr then browse through the result. The app uses an ansynchronous method to invoke a Flickr web service. The Flickr Viewer app allows user to search by _tag_ for photos that users worldwide have uploaded to Flickr. To access the Flickr web service on your computer, you must obtain your own Flickr API key at

http://www.flickr.com/services/apps/create/apply

and use it to replace the words YOUR API KEY HERE inside the program.

You are going to invoke the Flickr web service's method flickr.photos.search. You can learn more about this web-service method's parameters and the format of the URL for invoking the method at

https://www.flickr.com/services/api/flickr.photos.search.html

In this program, you specify values for the following parameters:

*   **api_key** (Required)
*   **tags**

    <dl>

    <dd>A comma-delimited list of tags. Photos with one or more of the tags listed will be returned. You can exclude results that match a term by prepending it with a - character.</dd>

    </dl>

*   **tag_mode**

    <dl>

    <dd>Either 'any' for an OR combination of tags, or 'all' for an AND combination. Defaults to 'any' if not specified.</dd>

    </dl>

*   **per_page**

    <dl>

    <dd>Number of photos to return per page. If this argument is omitted, it defaults to 100\. The maximum allowed value is 500.</dd>

    </dl>

*   **privacy_filter** (Optional)

    <dl>

    <dd id="yui_3_11_0_1_1458612447224_325">Return photos only matching a certain privacy level. This only applies when making an authenticated call to view photos you own. Use value 1.</dd>

    </dl>

The method flickr.photos.search returns the standard photo list xml:

<photos page="2" pages="89" perpage="10" total="881">  
<photo id="2636" owner="47058503995@N01"  
secret="a123456" server="2" title="test_04"  
ispublic="1" isfriend="0" isfamily="0" />  
<photo id="2635" owner="47058503995@N01"  
secret="b123456" server="2" title="test_03"  
ispublic="0" isfriend="1" isfamily="1" />  
<photo id="2633" owner="47058503995@N01"  
secret="c123456" server="2" title="test_01"  
ispublic="1" isfriend="0" isfamily="0" />  
<photo id="2610" owner="12037949754@N01"  
secret="d123456" server="2" title="00_tall"  
ispublic="1" isfriend="0" isfamily="0" />  
</photos>

**REST Request Format**

REST is the simplest request format to use - it's a simple HTTP GET or POST action.

The REST Endpoint URL is https://api.flickr.com/services/rest/

To request the flickr.test.echo service, invoke like this:

<pre>https://api.flickr.com/services/rest/?**method**=**flickr.test.echo**&**name**=**valu**e</pre>

The [partial code file](FlickrViewer.zip) (zip) for Window form.

If you to use WPF and MVVM pattern, you will get an extra credit of 15 points.

**Grading**

*   Demonstrate the solution to the instructor in the lab.
*   Submit the lab asssignment to BeachBoard
