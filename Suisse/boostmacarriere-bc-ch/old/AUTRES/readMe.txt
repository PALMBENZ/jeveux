Super choix. Voilà un pack clé-en-main Google Apps Script → Google Sheets → Gmail pour que ton formulaire envoie les données (et le CV) et te mail automatiquement.

1) Ce que j’ai déjà fait dans ta page

J’ai remplacé l’action="mailto:" par un envoi via fetch vers un endpoint Apps Script (placeholder SCRIPT_URL à remplacer).

Le formulaire envoie les champs Nom, Email, Téléphone, Objectifs + le fichier cv en multipart/form-data.

Un message d’état s’affiche (“Envoi…”, puis succès/erreur).

Tu n’as plus qu’à brancher l’URL Apps Script ci-dessous.



2) Créer le Google Sheet

Dans Google Drive → Nouveau > Google Sheets → nomme-le : CareerBoost_Leads.

Ligne 1 (entêtes) :
Horodatage | Nom | Email | Téléphone | Objectifs | FichierCV | Source | IP

(Les noms exacts n’ont pas besoin d’être identiques, mais je les utilise dans le script.)


3) Script Apps Script (colle tout dans l’éditeur Apps Script)

Dans Sheets : Extensions > Apps Script.

Remplace le contenu par ce code :