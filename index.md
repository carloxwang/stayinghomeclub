# Who's staying home because of COVID-19?

This is the running list of what in tech has been affected by COVID-19. Pull requests gratefully accepted, especially around design or data formatting or correctness. If you are a journalist and would like to speak to someone about the list, email phildini@phildini.net. <a href="https://github.com/phildini/stayinghomeclub/blob/master/README.md">Instructions for contributing are here</a>.

> 請注意這是一個台灣的版本，只允許有在台灣設有辦公室的公司

---

Jump to: <a href="/stayinghomeclub/companies.html">Companies</a>. 

---

<a name="companies"></a>
## [Companies - {{ site.data.companies | size }}](/stayinghomeclub/companies.html)
{% assign sorted = site.data.companies | sort %}
{% assign wfh_required = site.data.companies | where_exp:"item", "item.wfh contains 'Required'" | size %}
{% assign wfh_encouraged = site.data.companies | where_exp:"item", "item.wfh contains 'Encouraged'" | size %}

*Work from home required: **{{ wfh_required}}**, Work from home encouraged: **{{ wfh_encouraged }}***

### [See full list of companies](/stayinghomeclub/companies.html)

