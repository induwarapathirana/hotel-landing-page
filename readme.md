Aura Hotel Template: Customization GuideThis guide will walk you through the key sections of the aura-hotel-pitch.html file so you can quickly adapt it for any hotel you're pitching.

1. Branding & Identity
This is the first and most important step to personalizing the template.Hotel Name (AURA)Your hotel name appears in the navigation bar (logo area) and the global footer.Location: Search for AURA in the HTML.Lines to edit (approx. 106 & 768):<!-- In <nav> (Header) -->
<a href="#" class="nav-link text-2xl font-bold active" data-target="home">AURA</a>

<!-- In <footer> (Footer) -->
<p class="text-lg font-bold text-slate-800 dark:text-slate-200 mb-2">AURA</p>
Action: Replace AURA with your new hotel's name.Footer DetailsLocation: Find the <!-- ===== Global Footer ===== --> section (around line 766).Lines to edit (approx. 769-770):<p class="mb-4">123 Serenity Road, Coastline, CA 90210</p>
...
<p class="text-sm">&copy; <span id="current-year">2025</span> Aura Hotel Group. All rights reserved.</p>
Action: Change the address and the "Aura Hotel Group" text.2. The "Live Experience" (Home Page)This is the core of your pitch. You can customize the dynamic messages and the background video.Background VideoLocation: Find the <!-- ===== PAGE: Home ===== --> section (around line 186).Line to edit (approx. 191):<video autoplay loop muted playsinline poster="...">
    <source src="[https://videos.pexels.com/video-files/8044702/8044702-hd_1920_1080_25fps.mp4](https://videos.pexels.com/video-files/8044702/8044702-hd_1920_1080_25fps.mp4)" type="video/mp4">
</video>
Action: Replace the src in the <source> tag with a link to your hotel's "hero" video. You should also update the poster image URL.Dynamic Greetings & StatusLocation: Go to the <script> tag at the bottom of the file (around line 850).Lines to edit (approx. 855-870):if (currentHour < 12) {
    // Morning (Before 12 PM)
    greetingEl.textContent = 'Good Morning.';
    statusTextEl.textContent = 'Breakfast is now being served at The Arbor.';
} else if (currentHour < 17) {
    // Afternoon (12 PM - 5 PM)
    greetingEl.textContent = 'Good Afternoon.';
    statusTextEl.textContent = 'Enjoy poolside service at The Solstice Pool.';
    ...
} else {
    // Evening (After 5 PM)
    greetingEl.textContent = 'Good Evening.';
    statusTextEl.textContent = 'Live jazz begins soon at The Onyx Bar.';
    ...
}
Action: Change the textContent for the greetingEl (Good Morning/Afternoon/Evening) and statusTextEl (the "what's happening now" message) to match the specific hotel's amenities.

3. Booking Integration
This is where you'd link to the hotel's actual booking engine.
Location: Find the <!-- ===== Booking Section: The "Integration" ===== --> (around line 237).Line to edit (approx. 279):<a href="[https://www.booking.com/](https://www.booking.com/)" target="_blank" rel="noopener noreferrer" class="...">
    Book on Booking.com
    ...
</a>
Action: Change the href from https://www.booking.com/ to the hotel's specific Booking.com link (or other booking engine). You can also change the button text from "Book on Booking.com".4. Page Content & ImagesAll pages (Home, Rooms, Gallery, About, Contact) use placeholder images from https://placehold.co.Action: Do a "Find and Replace" for https://placehold.co. Replace these URLs with high-quality images from the hotel.Example (from Rooms page, line 431):<!-- BEFORE -->
<img src="[https://placehold.co/800x600/171717/f1f5f9?text=Deluxe+King+Room](https://placehold.co/800x600/171717/f1f5f9?text=Deluxe+King+Room)" alt="Deluxe King Room" ...>

<!-- AFTER (example) -->
<img src="[https://your-hotel-cdn.com/images/deluxe-king-room.jpg](https://your-hotel-cdn.com/images/deluxe-king-room.jpg)" alt="Deluxe King Room" ...>
Text: All text content inside <p>, <h3>, and <h2> tags within each <main data-page="..."> section is placeholder text. Simply edit it directly in the HTML.5. Theme & Styling (Colors)The template's main accent color is cyan. You can easily change this.Action: Do a project-wide "Find and Replace".Find: cyanReplace with: indigo, blue, emerald, amber, etc. (any standard Tailwind color name).This will instantly change all buttons, links, icons, and highlights to your new theme color, adapting the site to the hotel's branding in seconds.