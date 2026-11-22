<script setup lang="ts">
import { computed, ref } from 'vue'

const menuOpen = ref(false)
const closeMenu = () => { menuOpen.value = false }
const activeFilter = ref('Tous')
const filters = ['Tous', 'Mariage', 'Naissance & baptême', 'Anniversaire', 'Cérémonie']
const models = [
  { id:'atelier', name:'L’Atelier', category:'Mariage', style:'Éditorial & minimaliste', description:'Une composition typographique délicate, des lignes fines et une élégance intemporelle.', tone:'sand', initials:'A & L', date:'SAMEDI 18 JUIN 2027', label:'COLLECTION SIGNATURE' },
  { id:'heritage', name:'Héritage', category:'Mariage', style:'Classique & raffiné', description:'Un esprit de papeterie traditionnelle revisité dans une mise en page contemporaine.', tone:'rose', initials:'M & E', date:'DIMANCHE 12 SEPTEMBRE 2027', label:'COLLECTION ESSENTIELLE' },
  { id:'premiers-jours', name:'Premiers jours', category:'Naissance & baptême', style:'Doux & lumineux', description:'Des détails tendres et une palette apaisante pour annoncer une merveilleuse nouvelle.', tone:'peach', initials:'Bienvenue', date:'NOTRE PLUS BELLE RENCONTRE', label:'COLLECTION DOUCEUR' },
  { id:'celebrer', name:'À célébrer', category:'Anniversaire', style:'Festif & élégant', description:'Une invitation pleine de caractère pour réunir ceux qui comptent autour d’un beau moment.', tone:'plum', initials:'LET’S CELEBRATE', date:'UNE JOURNÉE À PARTAGER', label:'COLLECTION FESTIVE' },
  { id:'tradition', name:'Tradition', category:'Cérémonie', style:'Culturel & délicat', description:'Un écrin sobre et soigné, personnalisable selon vos traditions et votre histoire.', tone:'olive', initials:'Une belle occasion', date:'AVEC JOIE ET ÉMOTION', label:'COLLECTION CÉLÉBRATION' },
  { id:'essentiel', name:'L’Essentiel', category:'Mariage', style:'Moderne & épuré', description:'Une invitation graphique qui laisse toute sa place à l’essentiel : votre événement.', tone:'ink', initials:'C & J', date:'LE GRAND JOUR APPROCHE', label:'COLLECTION CONTEMPORAINE' }
]
const visibleModels = computed(() => activeFilter.value === 'Tous' ? models : models.filter(model => model.category === activeFilter.value))
const contactHref = (model: typeof models[number]) => `/contact?modele=${encodeURIComponent(model.name)}&occasion=${encodeURIComponent(model.category)}`
</script>

<template>
  <div class="site-shell models-page">
    <header class="site-header">
      <a class="brand" href="/" aria-label="C by C, accueil" @click="closeMenu"><img class="brand-logo" src="https://raw.githubusercontent.com/chirelhalioua/c-by-c/main/images/logo-c-by-c.png" alt="C by C — Célébrations by Chirel"></a>
      <button class="menu-toggle" type="button" :aria-expanded="menuOpen" aria-label="Ouvrir le menu" @click="menuOpen = !menuOpen"><span></span><span></span></button>
      <nav class="main-nav" :class="{ 'is-open': menuOpen }" aria-label="Navigation principale">
        <a href="/" @click="closeMenu">Accueil</a>
        <a href="/occasions" @click="closeMenu">Les occasions</a>
        <a href="/modeles" aria-current="page" @click="closeMenu">Nos modèles</a>
        <a href="/formules" @click="closeMenu">Nos formules</a>
        <a class="nav-cta" href="/contact" @click="closeMenu">Contact <span>↗</span></a>
      </nav>
    </header>

    <main>
      <section class="models-hero">
        <span class="section-eyebrow">LE CATALOGUE C BY C</span>
        <h1>Des modèles à votre image.<br><em>Une histoire à personnaliser.</em></h1>
        <p>Découvrez quelques univers imaginés pour vos beaux moments. Choisissez une inspiration, puis confiez-moi les détails pour en faire une création qui vous ressemble.</p>
        <span class="models-hero-note">DES CRÉATIONS NUMÉRIQUES · PERSONNALISABLES AVEC CŒUR</span>
      </section>

      <section class="models-catalogue section-pad" aria-label="Catalogue des modèles">
        <div class="models-toolbar">
          <div><span class="section-eyebrow">LA GALERIE</span><h2>Nos inspirations</h2></div>
          <div class="models-filters" aria-label="Filtrer les modèles">
            <button v-for="filter in filters" :key="filter" type="button" :class="{ 'is-active': activeFilter === filter }" @click="activeFilter = filter">{{ filter }}</button>
          </div>
        </div>

        <div class="models-grid">
          <article v-for="(model, index) in visibleModels" :key="model.id" class="model-card">
            <div class="model-preview" :class="'tone-' + model.tone">
              <span class="model-preview-index">C BY C · {{ String(index + 1).padStart(2, '0') }}</span>
              <div class="model-paper">
                <span class="model-paper-label">{{ model.label }}</span>
                <span class="model-paper-rule"></span>
                <span class="model-paper-script">{{ model.initials }}</span>
                <span class="model-paper-title">{{ model.name }}</span>
                <span class="model-paper-rule model-paper-rule-short"></span>
                <span class="model-paper-date">{{ model.date }}</span>
                <span class="model-paper-footer">AVEC JOIE · CÉLÉBRONS ENSEMBLE</span>
              </div>
              <span class="model-preview-caption">APERÇU DU MODÈLE</span>
            </div>
            <div class="model-card-copy">
              <div class="model-card-heading"><div><span class="model-category">{{ model.category }}</span><h3>{{ model.name }}</h3></div><span class="model-card-number">0{{ index + 1 }}</span></div>
              <p class="model-style">{{ model.style }}</p>
              <p class="model-description">{{ model.description }}</p>
              <a class="model-customize" :href="contactHref(model)">Personnaliser ce modèle <span aria-hidden="true">↗</span></a>
            </div>
          </article>
        </div>
        <p v-if="visibleModels.length === 0" class="models-empty">De nouveaux modèles arrivent bientôt.</p>
      </section>

      <section class="models-cta">
        <span class="section-eyebrow">UNE AUTRE ENVIE EN TÊTE ?</span>
        <h2>Votre idée mérite<br><em>son propre écrin.</em></h2>
        <p>Vous avez une inspiration particulière ou souhaitez partir d’une page blanche ? Parlons de votre projet.</p>
        <a class="button button-gold" href="/contact">Créer une invitation sur mesure <span>↗</span></a>
      </section>
    </main>

    <footer class="site-footer">
      <div class="footer-main"><a class="footer-brand" href="/"><img src="https://raw.githubusercontent.com/chirelhalioua/c-by-c/main/images/logo-c-by-c.png" alt="C by C — Célébrations by Chirel"></a><p>Les moments qui nous unissent.<br><span>Invitations digitales imaginées avec cœur.</span></p></div>
      <div class="footer-bottom"><span>© {{ new Date().getFullYear() }} C by C — Célébrations by Chirel</span><nav class="footer-legal-links" aria-label="Liens utiles"><a href="/">Accueil</a><a href="/contact">Contact</a><a href="/mentions-legales">Mentions légales</a><a href="/confidentialite">Confidentialité</a><a href="/cgv">CGV</a></nav><span>FAIT AVEC CŒUR PAR CHIREL</span></div>
    </footer>
  </div>
</template>
