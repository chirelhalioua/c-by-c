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
        <span class="section-eyebrow">INFORMATIONS COMMERCIALES</span>
        <h1>Conditions générales de vente</h1>
        <p>C by C — Célébrations by Chirel</p>
      </header>
      <p class="cgv-intro">Retrouvez ci-dessous les conditions applicables aux prestations proposées par C by C. Sélectionnez chaque rubrique pour consulter son contenu.</p>
      <article class="legal-content cgv-accordion-list">
        <details class="cgv-accordion">
          <summary>1. Identité du prestataire<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Les présentes conditions générales de vente (CGV) s’appliquent aux prestations proposées sous le nom commercial <strong>C by C — Célébrations by Chirel</strong>, exploité par Chirel Halioua, entrepreneur individuel exerçant sous le régime de la micro-entreprise.</p>
          <ul>
            <li>Nom commercial : C by C</li>
            <li>Prestataire : Chirel Halioua</li>
            <li>SIREN : 132 222 050</li>
            <li>SIRET : 132 222 050 00016</li>
            <li>Adresse électronique : <a href="mailto:contact@chirelhalioua.fr">contact@chirelhalioua.fr</a></li>
          </ul>
          <p>Les coordonnées postales du prestataire figurent sur le devis et les documents contractuels remis au client. Les présentes CGV ne dispensent pas le prestataire de communiquer les informations d’identification légalement requises avant la conclusion du contrat.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>2. Objet et champ d’application<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Les présentes CGV définissent les conditions dans lesquelles C by C propose aux particuliers et, le cas échéant, aux professionnels, des prestations de conception et de réalisation d’invitations numériques et de sites internet personnalisés destinés à des événements privés ou professionnels.</p>
          <p>Elles s’appliquent à toute commande acceptée par le prestataire. Toute condition particulière figurant sur un devis signé prévaut sur les présentes CGV en cas de contradiction.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>3. Prestations proposées<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Selon le devis accepté, les prestations peuvent notamment comprendre la création graphique d’une invitation numérique, la personnalisation d’un modèle, la conception d’un site de célébration, l’intégration de textes, photographies et informations transmis par le client, ainsi que des fonctionnalités ou options précisées au devis.</p>
          <p>Le périmètre exact, les fonctionnalités, les éventuelles options, les livrables, les limites techniques, la durée de mise en ligne et les prestations de maintenance ou d’hébergement sont définis individuellement dans le devis. Toute prestation non expressément mentionnée au devis est exclue.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>4. Demande, devis et formation de la commande<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Le client présente son projet par le formulaire de contact ou par courrier électronique. Le prestataire peut demander des précisions afin d’évaluer les besoins et d’établir un devis personnalisé.</p>
          <p>Le devis précise notamment la prestation, son prix, les options retenues, les modalités de paiement et le délai prévisionnel. Il est valable pendant la durée qui y est indiquée ou, à défaut, pendant 30 jours à compter de son émission.</p>
          <p>La commande devient ferme après acceptation écrite du devis par le client et encaissement de l’acompte prévu à l’article 6. Le prestataire confirme la prise en charge de la commande par courrier électronique. Aucun travail n’est engagé avant ces étapes, sauf accord écrit différent.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>5. Prix et taxes<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Les prix sont établis sur devis, en euros. Le montant total et le traitement de la TVA applicable sont indiqués sur le devis avant l’acceptation de la commande. Les éventuelles prestations supplémentaires font l’objet d’un devis complémentaire accepté par le client avant leur réalisation.</p>
          <p>Les frais ou options qui ne figurent pas dans le devis initial ne peuvent être facturés sans l’accord préalable du client. Le prestataire indique sur chaque facture le régime de TVA effectivement applicable à son entreprise à la date de facturation.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>6. Modalités de paiement<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Sauf disposition différente indiquée au devis, le paiement est effectué par virement bancaire selon l’échéancier suivant :</p>
          <ul>
            <li>30 % du prix total à titre d’acompte à la validation de la commande ;</li>
            <li>70 % du solde avant la livraison finale ou la mise en ligne de la création.</li>
          </ul>
          <p>Le démarrage du projet intervient après réception de l’acompte et des éléments nécessaires à sa réalisation. La livraison finale, la remise des fichiers définitifs ou la mise en ligne intervient après paiement intégral du prix convenu.</p>
          <p>En cas de retard de paiement, le prestataire peut suspendre les travaux et la livraison après en avoir informé le client. Pour les clients consommateurs, aucun frais ou pénalité non prévu par la loi ne sera appliqué. Pour les clients professionnels, les pénalités de retard et l’indemnité forfaitaire de recouvrement prévues par la réglementation sont exigibles dans les conditions légales.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>7. Délais et déroulement de la réalisation<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Le délai de réalisation est indiqué à titre prévisionnel dans le devis. Il commence à courir lorsque le prestataire dispose de l’acompte, du devis accepté et de l’ensemble des contenus et informations nécessaires (textes, visuels, choix graphiques et autres éléments demandés).</p>
          <p>Le client s’engage à transmettre des éléments exacts et définitifs dans des délais raisonnables et à répondre aux demandes de validation. Tout retard dans la transmission des éléments ou des retours peut entraîner un décalage du calendrier, sans que la responsabilité du prestataire puisse être engagée pour ce seul motif.</p>
          <p>Si un événement est prévu à une date déterminée, le client doit le signaler dès la demande de devis. Le calendrier correspondant doit être expressément accepté par le prestataire et indiqué au devis.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>8. Modifications et validation<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Sauf mention contraire au devis, deux séries de demandes de modifications sont incluses dans le prix. Une série correspond à un retour regroupé et transmis en une seule fois par le client.</p>
          <p>Les demandes doivent rester cohérentes avec le brief et la prestation initialement acceptée. Les changements importants de direction artistique, l’ajout de pages ou de fonctionnalités, la réécriture complète des contenus ou toute demande dépassant les deux séries incluses peuvent faire l’objet d’un devis complémentaire.</p>
          <p>Le prestataire soumet les éléments au client pour validation. Le client est responsable de la vérification attentive des textes, dates, horaires, adresses, liens, noms et autres informations avant validation finale.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>9. Obligations et contenus fournis par le client<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Le client garantit disposer des droits et autorisations nécessaires sur les textes, photographies, logos, musiques et autres éléments qu’il transmet. Il demeure responsable de leur exactitude, de leur licéité et du respect des droits des tiers, notamment du droit à l’image et des droits de propriété intellectuelle.</p>
          <p>Le prestataire peut refuser ou retirer tout contenu manifestement illicite, portant atteinte aux droits d’un tiers ou contraire à l’ordre public. Le client s’engage à collaborer de bonne foi et à fournir les informations nécessaires à la bonne exécution de la prestation.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>10. Livraison, mise en ligne et hébergement<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Les modalités de livraison sont précisées au devis : lien de consultation, fichier numérique, accès au site ou autre livrable convenu. Lorsque la prestation comprend un site en ligne, le devis précise, le cas échéant, la durée d’hébergement ou de disponibilité, le nom de domaine, les éventuels frais de services tiers et les conditions de renouvellement.</p>
          <p>Sauf mention expresse au devis, la maintenance continue, les mises à jour après livraison, les modifications ultérieures, le renouvellement d’un nom de domaine et les abonnements à des services tiers ne sont pas inclus.</p>
          <p>Le client est informé que la disponibilité d’un site peut dépendre de prestataires techniques tiers. Le prestataire ne peut garantir une disponibilité ininterrompue de services qu’il ne contrôle pas, mais s’engage à traiter les difficultés qui relèvent de son intervention dans un délai raisonnable.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>11. Droit de rétractation des consommateurs<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Lorsque le client est un consommateur et que le contrat est conclu à distance, il dispose en principe d’un délai de 14 jours pour exercer son droit de rétractation, sans avoir à motiver sa décision. Pour une prestation de services, ce délai court à compter de la conclusion du contrat.</p>
          <p>Pour exercer ce droit, le client peut adresser, avant l’expiration du délai, une déclaration dénuée d’ambiguïté à <a href="mailto:contact@chirelhalioua.fr">contact@chirelhalioua.fr</a>, en indiquant son nom, ses coordonnées et sa décision de se rétracter. Il peut également utiliser le formulaire type ci-dessous.</p>
          <p>Si le client souhaite que la prestation commence avant la fin du délai de rétractation, il doit en faire la demande expresse. En cas de rétractation après le début de la prestation, il peut être redevable du montant correspondant au service effectivement fourni jusqu’à la communication de sa décision, dans les conditions prévues par la loi. Lorsque la prestation a été pleinement exécutée avant la fin du délai, le droit de rétractation ne peut être perdu que si le client a donné son accord préalable exprès et reconnu qu’il perdrait ce droit après exécution complète.</p>
          <p>Pour un contenu numérique fourni sans support matériel, les règles spécifiques de renonciation au droit de rétractation ne s’appliquent que si les conditions légales sont réunies, notamment le consentement préalable exprès du client au commencement de l’exécution, sa reconnaissance de la perte de son droit et la confirmation du contrat par le professionnel.</p>
          <p><strong>Modèle de formulaire de rétractation :</strong><br>À l’attention de C by C — contact@chirelhalioua.fr<br>Je vous notifie par la présente ma rétractation du contrat portant sur la prestation suivante : …<br>Commandée le : …<br>Nom du consommateur : …<br>Adresse du consommateur : …<br>Date : …<br>Signature (uniquement en cas de notification sur papier) : …</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>12. Annulation et interruption du projet<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Toute demande d’annulation doit être adressée par écrit à <a href="mailto:contact@chirelhalioua.fr">contact@chirelhalioua.fr</a>. Les conséquences financières sont déterminées dans le respect du droit de rétractation lorsqu’il s’applique et des règles légales applicables au contrat.</p>
          <p>En dehors du droit légal de rétractation, si le client souhaite interrompre le projet après son démarrage, les parties établissent un état des travaux réalisés et des sommes déjà versées. Les prestations effectivement réalisées et les frais engagés et justifiés peuvent être facturés. Toute somme restant due ou à restituer est déterminée au regard du devis, de l’avancement réel et des dispositions légales applicables. L’acompte ne constitue pas une somme automatiquement acquise en toute circonstance.</p>
          <p>Si le prestataire ne peut poursuivre la prestation pour un motif qui lui est imputable, il en informe le client et rembourse les sommes correspondant aux prestations non réalisées, sans préjudice des droits que le client tient de la loi.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>13. Propriété intellectuelle<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Les créations originales, maquettes, éléments graphiques, modèles, méthodes et composants développés par le prestataire restent protégés par le droit de la propriété intellectuelle. Le paiement intégral de la commande confère au client uniquement les droits d’utilisation expressément prévus au devis ou dans un accord écrit distinct.</p>
          <p>Sauf cession écrite précisant les droits cédés, leur durée, leur territoire et leurs supports, aucun transfert général des droits de propriété intellectuelle n’est présumé. Les polices, images, extensions, logiciels et autres ressources de tiers restent soumis à leurs propres licences.</p>
          <p>Le prestataire ne réutilise pas les contenus personnels du client à des fins de communication ou de portfolio sans son autorisation préalable.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>14. Responsabilité<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Le prestataire s’engage à réaliser la prestation avec soin et conformément au devis accepté. Il ne saurait être tenu responsable des erreurs présentes dans les informations fournies ou validées par le client, ni des conséquences d’une utilisation du livrable non conforme à sa destination ou aux indications communiquées.</p>
          <p>Le prestataire ne garantit pas les résultats liés à des services tiers, aux réseaux de communication ou aux équipements du client. Aucune stipulation des présentes CGV n’a pour effet d’exclure ou de limiter une responsabilité qui ne peut légalement l’être, ni les droits impératifs reconnus aux consommateurs.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>15. Données personnelles<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Les données personnelles nécessaires à l’étude des demandes, à l’établissement des devis, à la gestion des commandes et au suivi des prestations sont traitées conformément à la politique de confidentialité accessible sur le site. Le client peut exercer ses droits dans les conditions qui y sont indiquées, notamment à l’adresse <a href="mailto:contact@chirelhalioua.fr">contact@chirelhalioua.fr</a>.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>16. Réclamations et médiation de la consommation<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Pour toute question ou réclamation, le client peut contacter le prestataire à l’adresse <a href="mailto:contact@chirelhalioua.fr">contact@chirelhalioua.fr</a>. Une solution amiable sera recherchée en priorité.</p>
          <p>Conformément au Code de la consommation, le consommateur peut, après avoir adressé une réclamation écrite préalable au prestataire et en l’absence de solution amiable, saisir gratuitement le médiateur de la consommation dont relève le prestataire.</p>
          <p><strong>Les coordonnées du médiateur de la consommation (nom, adresse postale et site internet) doivent être ajoutées ici avant toute conclusion de contrat avec un consommateur.</strong> Le prestataire doit adhérer à un dispositif de médiation compétent et communiquer ces coordonnées dans les CGV et les documents contractuels.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>17. Droit applicable et litiges<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Les présentes CGV sont soumises au droit français. En cas de litige avec un consommateur, les règles légales de compétence territoriale s’appliquent et le consommateur peut saisir la juridiction compétente conformément aux dispositions du Code de la consommation et du Code de procédure civile. Pour les clients professionnels, les règles de compétence applicables sont celles prévues par le droit commun, sous réserve des dispositions impératives.</p>
                  </div>
        </details>

        <details class="cgv-accordion">
          <summary>18. Acceptation et mise à jour des CGV<span class="cgv-accordion-icon" aria-hidden="true"></span></summary>
          <div class="cgv-accordion-content">
          <p>Le client reconnaît avoir pu prendre connaissance des présentes CGV avant l’acceptation du devis. Le prestataire peut les modifier pour l’avenir. Les CGV applicables à une commande sont celles communiquées au client et acceptées au moment de la conclusion du contrat.</p>
                  </div>
        </details>
      </article>
      <p class="legal-updated">Dernière mise à jour : novembre 2026.</p>
    </main>

    <footer class="site-footer">
      <div class="footer-main"><a class="footer-brand" href="/"><img src="https://raw.githubusercontent.com/chirelhalioua/c-by-c/main/images/logo-c-by-c.png" alt="C by C — Célébrations by Chirel"></a><p>Les moments qui nous unissent.<br><span>Invitations digitales imaginées avec cœur.</span></p></div>
      <div class="footer-bottom"><span>© {{ new Date().getFullYear() }} C by C — Célébrations by Chirel</span><nav class="footer-legal-links" aria-label="Liens utiles et réglementaires"><a href="/">Accueil</a><a href="/contact">Contact</a><a href="/mentions-legales">Mentions légales</a><a href="/confidentialite">Confidentialité</a><a href="/cgv">CGV</a></nav><span>FAIT AVEC CŒUR PAR CHIREL</span></div>
    </footer>
  </div>
</template>

<style scoped>
.cgv-intro {
  max-width: 760px;
  margin: 0 auto 1.5rem;
  color: var(--text-muted, #716b70);
  line-height: 1.7;
}
.cgv-accordion-list {
  display: grid;
  gap: 0.8rem;
}
.cgv-accordion {
  overflow: hidden;
  border: 1px solid rgba(91, 57, 78, 0.16);
  border-radius: 18px;
  background: rgba(255, 255, 255, 0.72);
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}
.cgv-accordion[open] {
  border-color: rgba(91, 57, 78, 0.38);
  box-shadow: 0 8px 24px rgba(55, 35, 48, 0.06);
}
.cgv-accordion summary {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1.25rem;
  padding: 1.15rem 1.35rem;
  color: inherit;
  font: inherit;
  font-weight: 650;
  line-height: 1.45;
  list-style: none;
  cursor: pointer;
}
.cgv-accordion summary::-webkit-details-marker {
  display: none;
}
.cgv-accordion summary:focus-visible {
  outline: 3px solid rgba(130, 94, 133, 0.45);
  outline-offset: -4px;
  border-radius: 16px;
}
.cgv-accordion-icon {
  position: relative;
  flex: 0 0 26px;
  width: 26px;
  height: 26px;
  border: 1px solid rgba(91, 57, 78, 0.22);
  border-radius: 50%;
}
.cgv-accordion-icon::before,
.cgv-accordion-icon::after {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 9px;
  height: 1.5px;
  border-radius: 2px;
  background: currentColor;
  content: "";
  transform: translate(-50%, -50%);
}
.cgv-accordion-icon::after {
  transform: translate(-50%, -50%) rotate(90deg);
  transition: transform 0.2s ease;
}
.cgv-accordion[open] .cgv-accordion-icon::after {
  transform: translate(-50%, -50%) rotate(0);
}
.cgv-accordion-content {
  padding: 0 1.35rem 1.3rem;
  color: inherit;
  line-height: 1.75;
}
.cgv-accordion-content p:first-child {
  margin-top: 0.15rem;
}
.cgv-accordion-content h3 {
  margin-top: 1rem;
}
@media (max-width: 640px) {
  .cgv-accordion summary {
    padding: 1rem;
    font-size: 0.96rem;
  }
  .cgv-accordion-content {
    padding: 0 1rem 1.1rem;
  }
}
</style>
