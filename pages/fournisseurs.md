---

layout: breadcrumbs
permalink: /fournisseurs
title: Fournisseurs et Partenaires
description: Tous les acteurs engagés dans le projet Bocauthèque
breadcrumbs:
  
---


# Fournisseurs et Partenaires


Ils sont gentils et tous du coin


<table class="collection-list">
  <thead>
    <tr>
      <th>Fournisseur</th>
      <th>Nom</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    {% assign fournisseurs = site.fournisseurs | sort: "sortOrder" %}
    {% for fournisseur in fournisseurs %}
      <tr class="collection-list-entry">
          <td class="table-pic">
         <a href="{{ site.baseurl }}{{ fournisseur.url }}" title="Tout à propos de {{ fournisseur.name }}"> 
            <img loading="lazy"   src="{{ fournisseur.logo }}" alt="Image de {{ fournisseur.name }}"> 
         </a>
          </td>
          <td>
              <a href="{{ site.baseurl }}{{ fournisseur.url }}" title="Tout à propos de {{ fournisseur.name }}"> {{ fournisseur.name }} </a>
          </td>
          <td class="overview">{{fournisseur.description}}</td>
          </tr>
    {% endfor %}
  </tbody>
</table>

