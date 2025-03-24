Warning!

Comparing to my YouTube video, I had to change my code a bit because some browsers (especially Safari on iOS) block continuous geolocation tracking.

Changes made:
I changed the tile provider and used CartoDB:
L.tileLayer("https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png", {
  attribution: "© OpenStreetMap & CartoDB contributors",
}).addTo(map);

I put all of the tracking logic inside the findLocation function. I call that function when the page loads, but I also added the "FIND ME" button, on which click I also call this function.

These changes should ensure the proper working of the app. 
If you still can't get your location (or find yourself in the middle of Atlantic) check Settings > Privacy & Security > Location Services and see if the app has location access.
