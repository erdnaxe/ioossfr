---
layout: page
title: Biographies
permalink: /biographies/
---

# Biographies des Iooss

{% for perso in site.data.iooss %}
<div class="media">
    <div class="media-left">
        {% if perso.pic %}<img src="{{ "/assets/pic/" | append: perso.pic | absolute_url }}" alt="Portrait">{% endif %}
        {% unless perso.pic %}<img src="{{ "/assets/pic/unknown.jpg" | absolute_url }}" alt="Portrait">{% endunless %}
    </div>
    <div class="media-body">
        <u>{{ perso.prenom }} <b>{{ perso.nom }}</b></u><br />
        <i>{% unless perso.date_naissance %}?{% endunless %}{{ perso.date_naissance }}</i> - <i>{% unless perso.date_mort %}?{% endunless %}{{ perso.date_mort }}</i><br />
        {% if perso.parent_de %}Parent de {{ perso.parent_de }}<br />{% endif %}
        {% if perso.enfant_de %}Enfant de {{ perso.enfant_de }}<br />{% endif %}
        {% if perso.bio_perso %}<a href="{{ "/assets/bio/" | append: perso.bio_perso | absolute_url }}">Voir la biographie personnelle</a>{% endif %}
        {% if perso.bio_familiale %}<a href="{{ "/assets/bio/" | append: perso.bio_familiale | absolute_url }}">Voir la biographie familiale</a>{% endif %}
    </div>
</div>
{% endfor %}


# Biographies des Mazin

{% for perso in site.data.mazin %}
<div class="media">
    <div class="media-left">
        {% if perso.pic %}<img src="{{ "/assets/pic/" | append: perso.pic | absolute_url }}" alt="Portrait">{% endif %}
        {% unless perso.pic %}<img src="{{ "/assets/pic/unknown.jpg" | absolute_url }}" alt="Portrait">{% endunless %}
    </div>
    <div class="media-body">
        <u>{{ perso.prenom }} <b>{{ perso.nom }}</b></u><br />
        <i>{% unless perso.date_naissance %}?{% endunless %}{{ perso.date_naissance }}</i> - <i>{% unless perso.date_mort %}?{% endunless %}{{ perso.date_mort }}</i><br />
        {% if perso.parent_de %}Parent de {{ perso.parent_de }}<br />{% endif %}
        {% if perso.enfant_de %}Enfant de {{ perso.enfant_de }}<br />{% endif %}
        {% if perso.bio_perso %}<a href="{{ "/assets/bio/" | append: perso.bio_perso | absolute_url }}">Voir la biographie personnelle</a>{% endif %}
        {% if perso.bio_familiale %}<a href="{{ "/assets/bio/" | append: perso.bio_familiale | absolute_url }}">Voir la biographie familiale</a>{% endif %}
    </div>
</div>
{% endfor %}
