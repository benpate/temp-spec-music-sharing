# Music Sharing on the Fediverse

This is a follow up to a [discussion at the FediForum](https://n00q.net/blog/fedicamp-propsal/) (March 2024) about creating a music sharing service on the Fediverse - initially dubbed "FediCamp" by [@n00q](https://don.n00q.net/@n00q)

### Requirement: A Fediverse Server
First and foremost, we are talking about making a standalone [Fediverse server](https://fediverse.party) that would allow small bands to create profiles and share content with their followers on the Fediverse.

### Requirement: Band Profile Page

* Customizable colors and graphics
* Upload music and group into albums, including:
    * Album Artwork
    * Lyrics
    * Date and other metadata
    * Shareable URLs for albums/songs for fans to share on their own social media
* Stream uploaded music <- will need details on this
* Band photos and biographies
* Links to other band URLs
* Calendar of events, with locations and links to ticket sales (possibly Federated)
* Other social posts that show up on the Fediverse
    * Blog posts
    * Photos
    * Upcoming dates (see calendar)
    * Other recommended bands

### Requirement: Music Discovery Service

* A list or group fans can follow for information on bands they like
    * New bands to follow that match my musical taste
    * New releases
    * Show dates/locations
* Search bands by name, genre, hashtag

### Non-Goals

* Do not focus on paid downloads. This is not important to many bands.
* Do not focus on merchandise sales. Bands often have another provider for merch.

## Emissary
[Emissary](https://emissary.dev) is a toolkit for building social web applications.  This section explores using Emissary as the core library for this music sharing tool.

| Requirement         | Emissary | Status |
| ------------------- | -------- | ------ |
| **Band Profiles**   | Custom User Profiles are supported | READY. Will need custom profile |
| Custom colors       | Will need to add custom data to User profiles | Needs Work (small) |
| Genre and Tags      | May need custom fields to mark the band's genre and other social tags | Needs Work (small) |
| Upload music        | Audio/Video uploads will need some development | Needs Work (medium) | 
| Album artwork       | Albums will be custom templates. Should be straighforward. | Needs work (small) |
| Lyrics              | Ditto. | Needs Work (small) |
| Other metadata      | Ditto. | Needs Work (small) |
| Shareable URLs      | Every profile and page has shareable URL (and QR code) | READY |
| Music Streaming     | Will need to research streaming protocols | Needs Work (UNKNOWN) | 
| Band photos         | Image upload galleries are supported. Will customize | Needs Work (small) |
| Band bios           | Can be made using custom data in a User Profile | Needs Work (small) |
| External Links      | Profiles support external links | YES |
| Event Calendar      | Can be made using custom templates under a User Profile | Needs Work (medium) |
| Social Posts        | Multiple post types are supported, but may need to be customized | Needs Work (medium) | 
| **Music Discovery** | | |
| Search engine       | This could be large or small, depending on the scope.  If we're just searching a single site | Needs Work (large) |
| Social feed         | This likely requires a human operator to populate. We should discuss a process for doing this.  | Needs Discussion |

## Next Steps

* **Streaming** I need to research music streaming.  Can this be done with a simple .mp3 file, or do we require a streaming server?
* **Social Feed** A "social feed" could be very simple, or very complex, depending on how much human involvement we're expecting to have.
* **Money** I think bands should pay *something* towards hosting and bandwidth -- especially if they're streaming music.  Off the top of my head, I'm starting with $10/year for a profile and inclusion in the discovery list, $20/year for profile + uploads + streaming. For comparison BndCamp takes 10-15% (plus 5% transaction fee) of all transactions
* **Drawings** If we have rough agreement on the scope we're looking at, I'll try drawing up how some of this might look (pencil and paper, scanned and uploaded) for us to talk about.
