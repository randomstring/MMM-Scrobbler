# MMM-Scrobbler
This is an extension for the [MagicMirror](https://github.com/MichMich/MagicMirror). It displays your currently playing music from Spotify. To use this you need to have a Premium Spotify account and your own API key.

## Installation

1. Navigate into your MagicMirror's `modules` folder and execute `git clone https://github.com/randomstring/MMM-Spotify-Currently-Playing.git`.

2. A new folder will appear. Configure the module and you're done.

## Configuration

You need to have a premium Spotify account to request an API key. 

1. Create an [account](https://www.spotify.com/)

2. Request an [api key]() from Spotify. 

3. Start playing music via Spotify

## Module Usage

The entry in the `module array` in your `config.js` can look like the following. Only username and apikey are mandatory fields. All other fields have default values.

```
{
			
	module: 'MMM-Spotify-Currently-Playing',
	
	position: 'top_right',
	config: {

		username: 'Spotify username',
	
		apikey: 'Spotify api key',
	
		//time interval to search for new song (every 15 seconds)
		updateInterval: 15 * 1000,
		//how often should we try to retrieve a song if not listening
		delayCount: 5,
		//time interval to search for new song if the 5 times not listening is received.
		//set this to the same number as updateInterval to ignore this option	
		delayInterval: 120*1000,
		animationSpeed: 1000,
		showAlbumArt: true,
	    	showMetaData: true,
		//Determines the position of the meta text. Possible values: top, bottom, left, right
		alignment: "bottom", 
		}
	
}

# Thanks

This was forked from [MMM-Scrobbler](https://github.com/PtrBld/MMM-Scrobbler), who did all the hard work already. I just changed it to use the Spotify API.
