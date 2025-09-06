# Workflow n8n : Extraction de données bancaires depuis un PDF

## Description
Ce workflow permet d’extraire automatiquement les opérations bancaires à partir d’un relevé PDF et de les convertir en un fichier **CSV exploitable**.  
Il détecte les lignes de transaction (dates, montants, libellés), les transforme en données structurées et les sauvegarde dans un fichier `.csv`.

⚠️ **Note** : Ce workflow est fourni tel quel. Il devra probablement être adapté à votre propre banque ou format de relevé.

---

## Fonctionnement
1. **Lecture d’un PDF** contenant les relevés bancaires.  
2. **Extraction du texte** des fichiers.  
3. **Nettoyage et parsing** pour isoler les champs utiles :  
   - Date  
   - Date de valeur  
   - Montant  
   - Libellé  
   - Débit / Crédit  
4. **Conversion en CSV** pour analyse ou intégration dans un tableur.

---

## Utilisation
1. Importez le fichier JSON dans votre instance n8n.  
2. Placez vos fichiers PDF dans le dossier défini dans le nœud de lecture (`/inputs/finances/pdf/`).  
3. Adaptez les chemins de sortie (`.csv`) selon vos besoins.  
4. Lancez le workflow et récupérez vos données structurées.

---

## Limitations
- Conçu initialement pour un format bancaire spécifique → peut nécessiter des ajustements (regex, structure du texte, libellés).  
- Fonctionne avec des relevés PDF texte (pas des scans image).  

---

## Contribution
Ce workflow est partagé gratuitement.  
👉 Si vous l’utilisez et souhaitez soutenir ce travail, vous pouvez contribuer via buymeacoffee.com/carlyto74.
