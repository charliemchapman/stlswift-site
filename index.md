---
layout: default
---

<section class="home-intro" aria-labelledby="home-title">
    <div class="home-copy">
        <p class="kicker">St. Louis Apple Developer Meetup</p>
        <h1 id="home-title">STL Swift</h1>
        <p class="lede">A local group for Swift, iOS, and Apple platform developers in St. Louis.</p>
    </div>
    <div class="home-actions" aria-label="Primary links">
        <a href="https://join.slack.com/t/stlswift/shared_invite/zt-2yna9lcmr-hLc6t5UT9fHEvxSGoiMrwA" class="main-link">
            <img src="/assets/images/slack-logo.png" alt="" class="social-icon">
            Join Slack
        </a>
        <a href="https://lu.ma/stlswift" class="main-link main-link-secondary" target="_blank" rel="noopener">
            <img src="/assets/images/luma-logo.svg" alt="" class="social-icon">
            Events on Luma
        </a>
    </div>
</section>

<section class="meetup-photos" aria-label="Photos from recent STL Swift meetups">
    <img src="/assets/images/meetups/talk-night.jpeg" alt="A speaker presenting at an STL Swift meetup">
    <img src="/assets/images/meetups/group-meetup.jpeg" alt="STL Swift members gathered after a meetup">
    <img src="/assets/images/meetups/deep-dish-swift-2026.jpeg" alt="STL Swift members at a casual meetup">
</section>

<div class="home-sections">
    <section class="home-section">
        <p class="section-label">About</p>
        <h2>Apple developers in St. Louis.</h2>
        <p>We meet regularly to discuss iOS development, share knowledge, and connect with other developers. New and experienced Apple platform developers are welcome.</p>
    </section>

    <section class="home-section">
        <p class="section-label">Connect</p>
        <h2>Find us online.</h2>
        <div class="social-links">
            <a href="https://twitter.com/STL_Swift">
                <img src="/assets/images/twitter-logo.png" alt="" class="social-icon">
                Twitter
            </a>
            <a href="https://bsky.app/profile/stlswift.com">
                <img src="/assets/images/bluesky-icon.svg" alt="" class="social-icon">
                Bluesky
            </a>
            <a href="https://mastodon.social/@stlswift">
                <img src="/assets/images/mastodon-icon.png" alt="" class="social-icon">
                Mastodon
            </a>
            <a href="https://www.linkedin.com/company/stlswift/">
                <span class="social-icon linkedin-icon" aria-hidden="true">in</span>
                LinkedIn
            </a>
        </div>
    </section>
</div>

<style>
.home-intro {
    display: grid;
    grid-template-columns: minmax(0, 1fr) auto;
    gap: 2rem;
    align-items: end;
    padding-bottom: 2.2rem;
    border-bottom: 1px solid var(--line);
}

.kicker,
.section-label {
    margin: 0 0 0.65rem;
    color: var(--orange);
    font-size: 0.78rem;
    font-weight: 800;
    letter-spacing: 0.08em;
    text-transform: uppercase;
}

.lede {
    max-width: 640px;
    color: var(--muted);
    font-size: clamp(1.15rem, 2.4vw, 1.45rem);
    line-height: 1.45;
}

.home-actions {
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
    min-width: 190px;
}

.home-actions .main-link {
    width: 100%;
}

.meetup-photos {
    display: grid;
    grid-template-columns: 1.25fr 1fr;
    grid-template-rows: repeat(2, minmax(170px, 1fr));
    gap: 0.85rem;
    margin: 2.3rem 0;
}

.meetup-photos img {
    width: 100%;
    height: 100%;
    min-height: 0;
    object-fit: cover;
    border-radius: 8px;
    border: 1px solid rgba(23, 23, 23, 0.08);
    box-shadow: var(--shadow);
}

.meetup-photos img:first-child {
    grid-row: 1 / 3;
}

.home-sections {
    display: grid;
    grid-template-columns: minmax(0, 1.1fr) minmax(280px, 0.9fr);
    gap: 2.5rem;
    align-items: start;
    padding-top: 0.4rem;
}

.home-section {
    border-top: 3px solid var(--green);
    padding-top: 1.1rem;
}

.home-section:nth-child(2) {
    border-top-color: var(--blue);
}

.home-section p:last-child {
    margin-bottom: 0;
}

.linkedin-icon {
    display: inline-grid;
    place-items: center;
    border-radius: 5px;
    background: #0a66c2;
    color: white;
    font-size: 0.86rem;
    font-weight: 800;
    line-height: 1;
}

.events-list {
    margin: 2rem 0;
}
.event-card {
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: 8px;
    padding: 1.5rem;
    margin-bottom: 1.5rem;
    display: flex;
    gap: 1.5rem;
    align-items: flex-start;
    box-shadow: var(--shadow);
}
.event-content {
    flex: 1;
}
.event-image {
    width: 150px;
    flex-shrink: 0;
}
.event-image img {
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 8px;
}
.event-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 1rem;
    margin-bottom: 1rem;
}
.event-main {
    flex: 1;
}
.event-rsvp {
    flex-shrink: 0;
}
.event-rsvp .main-link {
    margin: 0;
    white-space: nowrap;
}
.event-date {
    color: var(--muted);
    font-size: 0.9rem;
    margin-bottom: 0.5rem;
}
.event-title {
    margin: 0 0 0.5rem 0;
}
.event-title a {
    color: var(--orange);
    text-decoration: none;
}
.event-title a:hover {
    text-decoration: underline;
}
.event-location {
    margin-bottom: 1rem;
    color: var(--muted);
}
.event-excerpt {
    color: var(--ink);
}
.event-links {
    display: flex;
    gap: 1rem;
    align-items: center;
}
.event-details-link {
    color: var(--blue);
    text-decoration: none;
}
.event-details-link:hover {
    text-decoration: underline;
}
.section-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1rem;
}
.section-header h2 {
    margin: 0;
}
.view-all-link {
    color: var(--blue);
    text-decoration: none;
    font-size: 0.9rem;
    padding: 0.5rem 1rem;
    border: 1px solid var(--blue);
    border-radius: 8px;
    transition: all 0.2s ease;
}
.view-all-link:hover {
    background-color: var(--blue);
    color: white;
}
@media (max-width: 760px) {
    .home-intro,
    .home-sections {
        grid-template-columns: 1fr;
    }

    .home-intro {
        align-items: stretch;
    }

    .home-actions {
        align-self: stretch;
        min-width: 0;
        width: auto;
    }

    .home-actions .main-link {
        width: auto;
    }

    .meetup-photos {
        grid-template-columns: 1fr;
        grid-template-rows: none;
    }

    .meetup-photos img,
    .meetup-photos img:first-child {
        grid-row: auto;
        aspect-ratio: 4 / 3;
    }

    .event-card {
        flex-direction: column;
    }
    .event-image {
        width: 100%;
    }
    .event-image img {
        width: 100%;
        height: 150px;
    }
    .event-header {
        flex-direction: column;
    }
    .event-rsvp {
        align-self: flex-start;
    }
}
</style>
