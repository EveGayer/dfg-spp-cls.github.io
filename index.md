---
layout: default
title: Schwerpunktprogramm Computational Literary Studies
lang: de
ref: index
---

Im Zentrum des SPP Computational Literary Studies sollen literarische Texte in einem weiten Sinn stehen. Sie sind bislang erheblich seltener quantitativ erforscht worden als nicht-literarische Texte und stellen für quantitative Verfahren eine Herausforderung dar, da sie besonders komplex sind, z.B. wegen ihrer Fiktionalität, der kreativen, ästhetisch motivierten Verwendung von Sprache und/oder des spezifischen Charakters literarischer Zeichen. Mit literarischen Texten wird häufig nicht explizit, sondern indirekt durch Geschichten und Bilder kommuniziert, und sie neigen zur Individualisierung und Hybridisierung von Stil, Themen und Formen. Aus den Eigenheiten des Untersuchungsgegenstands und dem Forschungsstand des emergenten Feldes ergeben sich eine Reihe von Problemfeldern: die Notwendigkeit der Domänenadaption von Werkzeugen zur Textanalyse; das Verhältnis von Norm und Abweichung; die Bestimmung von Gemeinsamkeiten und Unterschieden zwischen literarischen und nicht-literarischen Texten; Schwierigkeiten, einen Konsens bei der Annotation literaturwissenschaftlich relevanter Texteigenschaften zu finden; der Mangel an interpretatorischer Transparenz moderner formaler Modelle; die Notwendigkeit des Aufbaus von Referenzkorpora. Dieses Forschungspro- gramm lässt sich nur durch eine eng vernetzte interdisziplinäre und damit auch risikoreiche

Forschung bewältigen, an der Forschende aus der Literaturwissenschaft, den Digital Humanities, der Korpuslinguistik, der Computerlinguistik und der Informatik beteiligt sind. Ziel des Schwerpunktprogramms ist es, durch die systematische Bearbeitung von Grundlagenfragen und die eng koordinierte Entwicklung von best practices zur Konsolidierung dieses wachsen- den, internationalen Forschungsfeldes beizutragen, um auf interdisziplinär vernetzte Weise das Methodenspektrum zur Analyse literarischer Texte nachhaltig um innovative, dem Gegen- stand angemessene und neue Einsichten versprechende Verfahren zu erweitern.






------
{% assign posts=site.posts | where:"index", true %}

{% if posts.size > 0 %}
## Neuigkeiten

<ul class="posts">
{% for post in posts offset: 0 limit: 3 %}
    {% assign germanVersion = site.posts | where:"ref", post.ref | where:"lang", "de" %}
	{% if post.lang=="en" %}
		{% if germanVersion == empty %}
			{% include date.html date=post.date lang=post.lang %}
			{% include teaser.html post=post %}
		{% endif %}
	{% else %}
		{% include date.html date=post.date lang=post.lang %}
		{% include teaser.html post=post %}
	{% endif %}
  {% endfor %}
</ul>

<div style="clear:both;"></div>

{% endif %}

