<script setup lang="ts">
const menuOpen = ref(false)
const closeMenu = () => { menuOpen.value = false }
</script>

<template>
  <div class="site-shell legal-page">
    <header class="site-header">
      <a class="brand" href="/" aria-label="C by C, accueil" @click="closeMenu">
        <img class="brand-logo" src="https://raw.githubusercontent.com/chirelhalioua/c-by-c/main/images/logo-c-by-c.png" alt="C by C — Célébrations by Chirel">
      </a>
      <button class="menu-toggle" type="button" :aria-expanded="menuOpen" aria-label="Ouvrir le menu" @click="menuOpen = !menuOpen"><span></span><span></span></button>
      <nav class="main-nav" :class="{ 'is-open': menuOpen }" aria-label="Navigation principale">
        <a href="/" @click="closeMenu">Accueil</a>
        <a href="/occasions" @click="closeMenu">Les occasions</a>
        <a href="/formules" @click="closeMenu">Nos formules</a>
        <a class="nav-cta" href="/contact" @click="closeMenu">Contact <span>↗</span></a>
      </nav>
    </header>
    <main class="legal-main section-pad">
      <header class="legal-heading">
        <span class="section-eyebrow">VOS DONNÉES, EN TOUTE TRANSPARENCE</span>
        <h1>Politique de confidentialité</h1>
        <p>C by C — Célébrations by Chirel</p>
      </header>
      <article class="legal-content">
        <p>La présente politique explique comment C by C traite les données personnelles que vous transmettez lorsque vous utilisez le formulaire de contact du site. Le site ne propose actuellement ni création de compte client, ni espace personnel, ni espace invité.</p>

        <section>
          <h2>Responsable du traitement</h2>
          <p>Le responsable du traitement est <strong>Chirel Halioua</strong>, entrepreneur individuel exerçant sous le nom commercial C by C, joignable à <a href="mailto:contact@chirelhalioua.fr">contact@chirelhalioua.fr</a>.</p>
        </section>

        <section>
          <h2>Données collectées</h2>
          <p>Le formulaire peut recueillir les informations suivantes :</p>
          <ul>
            <li>votre prénom et votre nom ;</li>
            <li>votre adresse e-mail et, si vous le souhaitez, votre numéro de téléphone ;</li>
            <li>le type et la date de l’événement ;</li>
            <li>la formule, le budget et les options envisagés ;</li>
            <li>le message et les précisions que vous choisissez de communiquer ;</li>
            <li>les informations techniques nécessaires à la vérification anti-robot et à la sécurité du formulaire.</li>
          </ul>
          <p>Merci de ne pas transmettre de données sensibles ou d’informations qui ne sont pas nécessaires à votre demande.</p>
        </section>

        <section>
          <h2>Finalités et bases légales</h2>
          <p>Les données du formulaire sont utilisées pour recevoir et traiter votre demande, communiquer avec vous au sujet de votre événement et, si vous le souhaitez, préparer une proposition commerciale. Ce traitement repose sur les mesures précontractuelles prises à votre demande.</p>
          <p>Les données techniques de sécurité sont utilisées pour protéger le formulaire contre les envois automatisés et les abus. Ce traitement repose sur l’intérêt légitime de sécuriser le site et son formulaire.</p>
          <p>Les informations ne sont pas utilisées pour vous envoyer une newsletter ou des communications commerciales sans démarche distincte et base légale appropriée.</p>
        </section>

        <section>
          <h2>Caractère obligatoire des informations</h2>
          <p>Les champs signalés par un astérisque sont nécessaires au traitement de votre demande. Si vous ne les renseignez pas, l’envoi du formulaire pourra être impossible. Le numéro de téléphone, la formule, le budget et les options sont facultatifs.</p>
        </section>

        <section>
          <h2>Destinataires et prestataires</h2>
          <p>Les informations transmises sont destinées à Chirel Halioua afin de traiter votre demande. Elles sont également traitées, dans la mesure nécessaire à leurs services, par les prestataires techniques suivants :</p>
          <ul>
            <li><strong>Vercel</strong> : hébergement du site et traitement technique des requêtes ;</li>
            <li><strong>Brevo</strong> : acheminement du message vers l’adresse de contact et envoi d’un e-mail confirmant la réception de votre demande ;</li>
            <li><strong>Cloudflare Turnstile</strong> : vérification anti-robot du formulaire.</li>
          </ul>
          <p>Le formulaire ne stocke pas actuellement les demandes dans une base de données du site : les informations sont transmises par e-mail. Elles peuvent donc rester présentes dans les boîtes e-mail utilisées pour gérer les demandes et dans les systèmes des prestataires selon leurs propres durées de conservation.</p>
        </section>

        <section>
          <h2>Transferts hors de l’Union européenne</h2>
          <p>Certains prestataires utilisés par le site peuvent traiter des données depuis des pays situés en dehors de l’Espace économique européen, notamment les États-Unis. Le cas échéant, ces transferts doivent être encadrés par les mécanismes prévus par le RGPD, tels qu'une décision d’adéquation applicable ou des garanties contractuelles appropriées. Les conditions et garanties effectivement applicables dépendent des services et paramètres des comptes utilisés.</p>
        </section>

        <section>
          <h2>Durée de conservation</h2>
          <p>Lorsqu’aucune commande n’est conclue, les données de votre demande sont conservées pendant une durée maximale de trois ans à compter de votre dernier contact avec C by C, puis supprimées ou archivées uniquement si une obligation légale ou la défense de droits en justice le justifie.</p>
          <p>Si une commande est conclue, les données nécessaires à la gestion de la relation contractuelle et au respect des obligations légales et comptables peuvent être conservées pendant les durées prévues par la réglementation applicable.</p>
          <p>Les messages présents dans les boîtes e-mail et les données détenues par les prestataires doivent être supprimés selon ces durées et les possibilités offertes par les services concernés.</p>
        </section>

        <section>
          <h2>Vos droits</h2>
          <p>Dans les conditions prévues par la réglementation, vous pouvez demander l’accès à vos données, leur rectification, leur effacement ou la limitation de leur traitement. Vous pouvez également vous opposer à un traitement fondé sur l’intérêt légitime et demander la portabilité des données lorsque ce droit est applicable.</p>
          <p>Pour exercer vos droits ou poser une question sur vos données, écrivez à <a href="mailto:contact@chirelhalioua.fr">contact@chirelhalioua.fr</a>. Vous pouvez également introduire une réclamation auprès de la <a href="https://www.cnil.fr/" target="_blank" rel="noopener noreferrer">CNIL</a>.</p>
        </section>

        <section>
          <h2>Sécurité</h2>
          <p>C by C met en œuvre des mesures raisonnables pour protéger les informations reçues. Le formulaire utilise notamment une vérification anti-robot. Aucun mode de transmission ou de stockage ne pouvant garantir une sécurité absolue, évitez d’inclure des informations confidentielles ou sensibles dans votre message.</p>
        </section>

        <section>
          <h2>Cookies et traceurs</h2>
          <p>Le formulaire charge le service Cloudflare Turnstile pour sa vérification anti-robot. Ce service peut traiter des informations techniques relatives à votre navigateur et à votre interaction avec le formulaire afin de distinguer les visiteurs humains des robots. Pour plus d’informations, vous pouvez consulter la <a href="https://www.cloudflare.com/privacypolicy/" target="_blank" rel="noopener noreferrer">politique de confidentialité de Cloudflare</a> et la <a href="https://www.cloudflare.com/website-terms/" target="_blank" rel="noopener noreferrer">documentation juridique de Cloudflare</a>.</p>
          <p>Cette rubrique devra être mise à jour si des outils de mesure d’audience, de publicité ou d’autres traceurs sont ajoutés au site.</p>
        </section>

        <section>
          <h2>Mise à jour</h2>
          <p>Cette politique peut être modifiée en cas d’évolution du formulaire, des prestataires utilisés ou de la réglementation. La date de mise à jour figurera sur cette page.</p>
        </section>
      </article>
      <p class="legal-updated">Dernière mise à jour : novembre 2026.</p>
    </main>
    <footer class="site-footer">
      <div class="footer-main"><a class="footer-brand" href="/"><img src="https://raw.githubusercontent.com/chirelhalioua/c-by-c/main/images/logo-c-by-c.png" alt="C by C — Célébrations by Chirel"></a><p>Les moments qui nous unissent.<br><span>Invitations digitales imaginées avec cœur.</span></p></div>
      <div class="footer-bottom"><span>© {{ new Date().getFullYear() }} C by C — Célébrations by Chirel</span><nav class="footer-legal-links" aria-label="Liens utiles"><a href="/">Accueil</a><a href="/contact">Contact</a><a href="/mentions-legales">Mentions légales</a><a href="/confidentialite">Confidentialité</a><a href="/cgv">CGV</a></nav><span>FAIT AVEC CŒUR PAR CHIREL</span></div>
    </footer>
  </div>
</template>
