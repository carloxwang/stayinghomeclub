# Who's staying home because of COVID-19?

This is the running list of what in tech has been affected by COVID-19. Pull requests gratefully accepted, especially around design or data formatting or correctness. If you are a journalist and would like to speak to someone about the list, email phildini@phildini.net. <a href="https://github.com/phildini/stayinghomeclub/blob/master/README.md">Instructions for contributing are here</a>.

> 請注意這是一個台灣的版本，只允許有在台灣設有辦公室的公司

---

Jump to: <a href="/stayinghomeclub/companies.html">Companies</a>. Jump to: <a href="/stayinghomeclub/events.html">Events</a>. Jump to: <a href="/stayinghomeclub/universities.html">Universities</a>.

---

<a name="companies"></a>
## [Companies - {{ site.data.companies | size }}](/stayinghomeclub/companies.html)
{% assign sorted = site.data.companies | sort %}
{% assign wfh_required = site.data.companies | where_exp:"item", "item.wfh contains 'Required'" | size %}
{% assign wfh_encouraged = site.data.companies | where_exp:"item", "item.wfh contains 'Encouraged'" | size %}

*Work from home required: **{{ wfh_required}}**, Work from home encouraged: **{{ wfh_encouraged }}***

### [See full list of companies](/stayinghomeclub/companies.html)

---

<a name="events"></a>
{% assign cancelled = site.data.events | where_exp:"item", "item.status contains 'cancelled'" | size %}

## [Events - {{ site.data.events | size }}](/stayinghomeclub/events.html)

*Events cancelled: **{{cancelled}}***

### [See full list of events](/stayinghomeclub/events.html)

---

<a name="universities"></a>

## [Universities -- {{ site.data.universities | size }}](/stayinghomeclub/universities.html)

{% assign statuses = "" | split: "" %}
{% for university in site.data.universities %}
    {% assign status = university[1].status | downcase %}
    {% assign statuses = statuses | push: status %}
{% endfor %}
{% assign remote_count = statuses | where_exp:"status", "status contains 'remote'" | size %}
*Universities moving to remote teaching: **{{remote_count}}***

### [See full list of universities](/stayinghomeclub/universities.html)

---

Jump to: <a href="/stayinghomeclub/companies.html">Companies</a>. Jump to: <a href="/stayinghomeclub/events.html">Events</a>. Jump to: <a href="/stayinghomeclub/universities.html">Universities</a>.
