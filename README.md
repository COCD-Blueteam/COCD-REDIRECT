# COCD-REDIRECT

Page de redirection pour le consentement administrateur (Admin Consent) des App Registrations Azure AD.

## 🎯 Objectif

Cette GitHub Page sert d'URL de redirection (`redirect_uri`) pour les flux de consentement administrateur des applications Azure AD (Entra ID) globales.

## 🚀 URL de la page

Une fois GitHub Pages activé, la page sera accessible à :
```
https://[votre-username].github.io/COCD-REDIRECT/
```

## ⚙️ Configuration Azure AD

### 1. Dans votre App Registration Azure :

1. Allez sur le **Portail Azure** → **Azure Active Directory** → **App registrations**
2. Sélectionnez votre application
3. Allez dans **Authentication**
4. Ajoutez l'URL de redirection :
   ```
   https://[votre-username].github.io/COCD-REDIRECT/
   ```
5. Sélectionnez le type : **Web**
6. Sauvegardez

### 2. URL de consentement administrateur :

Utilisez cette URL pour demander le consentement :
```
https://login.microsoftonline.com/{tenant-id}/adminconsent?client_id={client-id}&redirect_uri=https://[votre-username].github.io/COCD-REDIRECT/
```

Remplacez :
- `{tenant-id}` : L'ID de votre tenant Azure AD
- `{client-id}` : L'ID client de votre App Registration

## 📋 Fonctionnalités

La page affiche automatiquement :

✅ **En cas de succès :**
- Message de confirmation
- Tenant ID
- Date et heure du consentement
- État (state) si fourni

❌ **En cas d'erreur :**
- Message d'erreur
- Description détaillée
- Tenant ID

ℹ️ **Accès direct :**
- Information sur l'utilisation de la page
- URL actuelle

## 🛠️ Activation de GitHub Pages

1. Allez dans les **Settings** de ce dépôt
2. Naviguez vers **Pages** (dans le menu latéral)
3. Sous **Source**, sélectionnez :
   - Branch : `main`
   - Folder : `/ (root)`
4. Cliquez sur **Save**
5. Attendez quelques minutes que la page soit déployée

## 🎨 Interface

- Design moderne et responsive
- Compatible mobile
- Animation fluide
- Couleurs professionnelles
- Interface bilingue (français)

## 📝 Paramètres URL gérés

La page détecte et traite automatiquement :
- `tenant` : ID du tenant Azure AD
- `admin_consent` : Statut du consentement (True/False)
- `state` : Paramètre d'état personnalisé
- `error` : Code d'erreur
- `error_description` : Description de l'erreur

## 🔒 Sécurité

Cette page ne collecte ni ne stocke aucune donnée. Elle affiche uniquement les paramètres reçus d'Azure AD dans le navigateur de l'utilisateur.

## 📞 Support

Pour toute question concernant cette page de redirection, veuillez contacter l'administrateur de l'application.

---

**COCD** - Azure App Registration Redirect Page

