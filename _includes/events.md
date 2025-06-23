
## Upcoming Events

{% assign today = 'now' | date: '%s' %}
{% assign bwaconf25off = '2025-07-12' | date: '%s' %}
{% assign bwaoday25off = '2025-07-09' | date: '%s' %}
{% assign bhsq2511off = '2025-11-02' | date: '%s' %}

{% if today < bwaconf25off %}
#### Brisbane self-guided walking tour: [download PDF](/pdf/Exploring-Baptist-Brisbane-2025-06-16.pdf) for guests at the BWA Conference Brisbane July 2025.
{% endif %}

{% if today < bwaoday25off %}
#### Baptist Archive Open Day for BWA participants: 9 July 2025. RSVP to [archives@qb.org.au](mailto:archives@qb.org.au?BWA%20Open%20Day).
{% endif %}


{% if page.menu == 'bhq' %}
{% if today < bhsq2511off %}
#### Next BHSQ meeting 2pm 1 November 2025. Baptist Archive.
{% endif %}
{% endif %}