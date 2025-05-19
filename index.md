---
layout: default
---

Welcome to STL Swift, the iOS developer meetup group in St. Louis! We're a community of developers passionate about Swift, iOS, and Apple platform development.

<a href="https://join.slack.com/t/stlswift/shared_invite/zt-2yna9lcmr-hLc6t5UT9fHEvxSGoiMrwA" class="main-link">
    <img src="/assets/images/slack-logo.png" alt="Slack" class="social-icon">
    Join our Slack Community
</a>

<div class="section-header">
    <h2>Upcoming Events</h2>
    <a href="/events" class="view-all-link">View All</a>
</div>

<div class="events-list">
{% assign future_events = site.events | where_exp:"event", "event.date > site.time" | sort: 'date' %}
{% if future_events.size > 0 %}
  {% for event in future_events %}
    <div class="event-card">
        {% if event.image %}
        <div class="event-image">
            <img src="{{ event.image }}" alt="{{ event.display_title | default: event.title }}">
        </div>
        {% endif %}
        <div class="event-content">
            <div class="event-header">
                <div class="event-main">
                    <div class="event-date">
                        {{ event.date | date: "%B %d, %Y at %I:%M %p" }}
                    </div>
                    <h3 class="event-title">
                        <a href="{{ site.baseurl }}{{ event.url }}">{{ event.display_title | default: event.title }}</a>
                    </h3>
                    {% if event.location %}
                    <div class="event-location">
                        📍 {{ event.location }}
                    </div>
                    {% endif %}
                </div>
                {% if event.rsvp_link %}
                <div class="event-rsvp">
                    <a href="{{ event.rsvp_link }}" class="main-link" target="_blank" rel="noopener">RSVP</a>
                </div>
                {% endif %}
            </div>
            <div class="event-excerpt">
                {{ event.content | strip_html | truncatewords: 50 }}
            </div>
        </div>
    </div>
  {% endfor %}
{% else %}
  <p>No upcoming events scheduled. Check back soon!</p>
{% endif %}
</div>

## Connect With Us

<div class="social-links">
<a href="https://twitter.com/stlswift">
    <img src="/assets/images/twitter-logo.png" alt="Twitter" class="social-icon">
    Twitter
</a>
<a href="https://bsky.app/profile/stlswift.bsky.social">
    <img src="/assets/images/bluesky-icon.svg" alt="Bluesky" class="social-icon">
    Bluesky
</a>
<a href="https://mastodon.social/@stlswift">
    <img src="/assets/images/mastodon-icon.png" alt="Mastodon" class="social-icon">
    Mastodon
</a>
</div>

## About Us

We meet regularly to discuss iOS development, share knowledge, and network with fellow developers. Whether you're just starting with Swift or you're an experienced developer, everyone is welcome to join our community!

<style>
.events-list {
    margin: 2rem 0;
}
.event-card {
    background: #f8f8f8;
    border-radius: 12px;
    padding: 1.5rem;
    margin-bottom: 1.5rem;
    display: flex;
    gap: 1.5rem;
    align-items: flex-start;
}
.event-content {
    flex: 1;
}
.event-image {
    width:150px;
    flex-shrink: 0;
}
.event-image img {
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
    color: #666;
    font-size: 0.9rem;
    margin-bottom: 0.5rem;
}
.event-title {
    margin: 0 0 0.5rem 0;
}
.event-title a {
    color: #FF3B30;
    text-decoration: none;
}
.event-title a:hover {
    text-decoration: underline;
}
.event-location {
    margin-bottom: 1rem;
    color: #666;
}
.event-excerpt {
    color: #333;
}
.event-links {
    display: flex;
    gap: 1rem;
    align-items: center;
}
.event-details-link {
    color: #007AFF;
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
    color: #007AFF;
    text-decoration: none;
    font-size: 0.9rem;
    padding: 0.5rem 1rem;
    border: 1px solid #007AFF;
    border-radius: 6px;
    transition: all 0.2s ease;
}
.view-all-link:hover {
    background-color: #007AFF;
    color: white;
}
@media (max-width: 600px) {
    .event-card {
        flex-direction: column;
    }
    .event-image {
    }
    .event-image img {
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