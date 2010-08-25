# simplenote-js

A JS wrapper for the SimpleNote API.  Routes all requests through
[YQL](http://developer.yahoo.com/yql/) (via HTTPS) using the included
Open Data table (see `src/` folder).  Needs jQuery.


## Usage

It's rather straightforward: first, authenticate, and if you've done so
successfully, go nuts.

    var s = new SimpleNote();
    s.auth({
      email: "test@example.com",
      password: "myPassword",
      success: function() {
        console.log( s.isLoggedIn() );
      },
      error: function( code ) {
        console.error( "Authentication error: " + code );
      }
    });
    
    …
    
    s.getIndex({
      success: function( data ) {
        console.info( data );
      },
      error: function( code ) {
        console.error( code );
      }
    });
    
    
## Requirements

* jQuery 1.4+


## Author

Carlo Zottmann, [municode.de](http://municode.de/), carlo@municode.de.  Nice
to meet you.


## License

Dual-license, MIT & GNU GPL v2.