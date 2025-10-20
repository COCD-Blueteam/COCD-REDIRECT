# COCD-REDIRECT

Page de redirection pour le consentement administrateur Azure AD.

---

## 🚀 Configuration Rapide

### 1. Modifier index.html

Ouvrez `index.html` et modifiez ces 2 lignes (environ ligne 262) :

```javascript
const CONFIG = {
    AUTHORIZED_DOMAIN: 'votre-username.github.io',  // ⚠️ Changez ici
    AUTHORIZED_PATH: '/COCD-REDIRECT'                // ⚠️ Vérifiez le nom
};
```

**Exemple :**
```javascript
const CONFIG = {
    AUTHORIZED_DOMAIN: 'johndoe.github.io',
    AUTHORIZED_PATH: '/COCD-REDIRECT'
};
```

### 2. Activer GitHub Pages

1. Allez dans **Settings** → **Pages**
2. Source : Branch `main`, Folder `/ (root)`
3. Cliquez sur **Save**
4. Attendez 2-3 minutes

**Votre URL sera :**
```
https://votre-username.github.io/COCD-REDIRECT/
```

### 3. Configurer Azure AD

Dans votre App Registration → **Authentication** :

Ajoutez cette Redirect URI :
```
https://votre-username.github.io/COCD-REDIRECT/
```

Type : **Web**

### 4. URL de consentement

```
https://login.microsoftonline.com/{tenant-id}/adminconsent?client_id={client-id}&redirect_uri=https://votre-username.github.io/COCD-REDIRECT/
```

Remplacez `{tenant-id}` et `{client-id}` par vos valeurs.

---

## ✅ C'est tout !

La page va :
- ✅ Afficher le succès/échec du consentement
- ✅ Détecter automatiquement si quelqu'un copie la page (affichera "Site non officiel")
- ✅ Afficher un disclaimer gouvernemental

---

## 🔒 Protection Anti-Copie

Si quelqu'un copie/fork cette page, elle détectera automatiquement qu'elle n'est pas sur le bon domaine et affichera un avertissement **"Site Non Officiel"**.

Vous n'avez rien à faire, c'est automatique une fois que vous avez configuré `AUTHORIZED_DOMAIN`.

---

## 🛡️ Désactiver les Forks (Optionnel)

Pour empêcher les forks via GitHub :

1. **Settings** → **General**
2. Décochez : ☐ "Allow forking"

---

## 📞 Support

Pour toute question, contactez votre administrateur système.

---

**COCD** - Entité Gouvernementale de Cybersécurité
