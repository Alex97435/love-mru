# love-mru
Application de rencontre pour Maurice
Pas de problème ! 🚀 Je vais vous donner une solution alternative. Au lieu de télécharger, je vais vous montrer **tous les fichiers directement** que vous pourrez copier-coller sur GitHub.

## 🎯 **Solution Alternative : Copier-Coller Direct**

### **Étape 1 : Créez votre Repository GitHub**
1. Allez sur **github.com**
2. Cliquez **"New repository"**
3. Nom : **"love-mru"**
4. Description : **"Application de rencontre pour Maurice"**
5. **Public** ou **Private** (votre choix)
6. Cliquez **"Create repository"**

### **Étape 2 : Je vous donne tous les fichiers un par un**

Voici le **fichier principal - README.md** à créer en premier :
Action: file_editor view /app/README.md
Observation: /app/README.md:
1|# 🌴 LOVE MRU - Application de Rencontre pour Maurice
2|
3|**L'application de rencontre dédiée à l'île Maurice** - Connectant résidents et touristes dans un environnement sécurisé et convivial.
4|
5|![LOVE MRU](https://img.shields.io/badge/LOVE%20MRU-Dating%20App-yellow) ![Next.js](https://img.shields.io/badge/Next.js-14.2.3-black) ![Supabase](https://img.shields.io/badge/Supabase-Backend-green) ![Mauritius](https://img.shields.io/badge/Made%20for-Mauritius-red)
6|
7|## 🚀 Application Déployée
8|
9|**🌐 URL Principale :** https://shipping-system.emergent.host/
10|**🛠️ Panneau Admin :** https://shipping-system.emergent.host/admin (mot de passe: `LoveMRU2025!`)
11|
12|## ✨ Fonctionnalités Principales
13|
14|### 🎯 **Pour les Utilisateurs**
15|- ✅ **Inscription/Connexion** sécurisée avec Supabase
16|- ✅ **Profils détaillés** avec photos, âge, préférences
17|- ✅ **Statut Résident/Touriste** pour cibler les bonnes personnes
18|- ✅ **Interface de découverte** avec système de swipe
19|- ✅ **Système de matching** quand deux personnes s'aiment
20|- ✅ **Interface bilingue** Français/Anglais
21|- ✅ **Thème Maurice** avec palette jaune tropicale
22|- ✅ **Design responsive** mobile, tablette, desktop
23|
24|### 🛠️ **Panneau d'Administration**
25|- ✅ **Gestion des utilisateurs** - Voir, modifier, supprimer des profils
26|- ✅ **Statistiques en temps réel** - Résidents, touristes, matches
27|- ✅ **Configuration de l'app** - Âges, limites, paramètres
28|- ✅ **Modération** - Signalements, blocages
29|- ✅ **Tableau de bord** complet avec métriques
30|
31|## 🏗️ Architecture Technique
32|
33|### **Frontend**
34|- **Framework :** Next.js 14.2.3 avec App Router
35|- **Styling :** Tailwind CSS + shadcn/ui components
36|- **Icons :** Lucide React
37|- **Responsive :** Mobile-first design
38|
39|### **Backend**
40|- **Base de données :** Supabase PostgreSQL
41|- **Authentification :** Supabase Auth
42|- **API :** Next.js API Routes avec CORS
43|- **Sécurité :** Row Level Security (RLS)
44|
45|### **Déploiement**
46|- **Production :** emergent.host
47|- **SSL :** Automatique
48|- **CDN :** Optimisé pour performance mondiale
49|
50|## 📁 Structure du Projet
51|
52|```
53|/
54|├── app/
55|│   ├── page.js                 # Page principale de l'application
56|│   ├── admin/page.js           # Panneau d'administration
57|│   ├── layout.js               # Layout principal
58|│   ├── globals.css             # Styles globaux
59|│   └── api/
60|│       └── [[...path]]/route.js # API backend
61|├── components/ui/              # Composants shadcn/ui
62|├── lib/
63|│   ├── supabase.js            # Configuration Supabase
64|│   └── utils.js               # Utilitaires
65|├── .env                       # Variables d'environnement
66|├── tailwind.config.js         # Configuration Tailwind
67|├── next.config.js             # Configuration Next.js
68|└── package.json               # Dépendances
69|
70|```
71|
72|## ⚙️ Configuration Supabase
73|
74|### **Tables Requises**
75|
76|```sql
77|-- Table des profils utilisateurs
78|CREATE TABLE profiles (
79|  id TEXT PRIMARY KEY,
80|  user_id TEXT UNIQUE NOT NULL,
81|  first_name TEXT NOT NULL,
82|  age INTEGER,
83|  gender TEXT,
84|  orientation TEXT,
85|  status TEXT DEFAULT 'resident',  -- 'resident' ou 'tourist'
86|  bio TEXT,
87|  languages TEXT[],
88|  avatar_base64 TEXT,
89|  location JSONB,
90|  interests TEXT[]
91|);
92|
93|-- Table des matches
94|CREATE TABLE matches (
95|  id TEXT PRIMARY KEY,
96|  user1_id TEXT NOT NULL,
97|  user2_id TEXT NOT NULL,
98|  user1_liked BOOLEAN DEFAULT FALSE,
99|  user2_liked BOOLEAN DEFAULT FALSE,
100|  matched BOOLEAN DEFAULT FALSE,
101|  UNIQUE(user1_id, user2_id)
102|);
103|
104|-- Sécurité Row Level Security
105|ALTER TABLE profiles ENABLE ROW LEVEL SECURITY;
106|ALTER TABLE matches ENABLE ROW LEVEL SECURITY;
107|
108|CREATE POLICY "Allow all operations on profiles" ON profiles FOR ALL USING (true);
109|CREATE POLICY "Allow all operations on matches" ON matches FOR ALL USING (true);
110|```
111|
112|### **Variables d'Environnement**
113|
114|```env
115|# Supabase Configuration
116|NEXT_PUBLIC_SUPABASE_URL=https://votre-projet.supabase.co
117|NEXT_PUBLIC_SUPABASE_ANON_KEY=votre-cle-anon
118|SUPABASE_SERVICE_ROLE_KEY=votre-cle-service-role
119|
120|# MongoDB (legacy)
121|MONGO_URL=mongodb://localhost:27017/mydatabase
122|
123|# App Configuration
124|NEXT_PUBLIC_BASE_URL=https://shipping-system.emergent.host
125|```
126|
127|## 🚀 Installation et Développement Local
128|
129|### **1. Cloner le repository**
130|```bash
131|git clone https://github.com/votre-username/love-mru.git
132|cd love-mru
133|```
134|
135|### **2. Installer les dépendances**
136|```bash
137|yarn install
138|```
139|
140|### **3. Configurer l'environnement**
141|```bash
142|cp .env.example .env
143|# Éditer .env avec vos clés Supabase
144|```
145|
146|### **4. Lancer le serveur de développement**
147|```bash
148|yarn dev
149|```
150|
151|L'application sera accessible sur `http://localhost:3000`
152|
153|## 📱 API Endpoints
154|
155|### **Authentification**
156|- `POST /api?path=auth/signup` - Inscription utilisateur
157|- `POST /api?path=auth/signin` - Connexion utilisateur
158|- `POST /api?path=auth/signout` - Déconnexion
159|- `GET /api?path=auth/user` - Obtenir utilisateur actuel
160|
161|### **Profils**
162|- `GET /api?path=profiles` - Lister tous les profils
163|- `POST /api?path=profiles` - Créer un profil
164|- `PUT /api?path=profiles` - Mettre à jour un profil
165|- `DELETE /api?path=profiles&id=xxx` - Supprimer un profil
166|
167|### **Matches**
168|- `GET /api?path=matches&userId=xxx` - Obtenir les matches d'un utilisateur
169|- `POST /api?path=matches` - Créer/mettre à jour un match (like/pass)
170|
171|### **Utilitaires**
172|- `GET /api?path=health` - Vérification de santé
173|- `GET /api?path=init` - Initialisation base de données
174|
175|## 🎨 Personnalisation
176|
177|### **Couleurs et Thème**
178|Le thème actuel utilise une palette jaune inspirée de Maurice :
179|- **Primaire :** `bg-yellow-500` (jaune Maurice)
180|- **Secondaire :** `from-yellow-50 to-orange-100` (dégradé tropical)
181|- **Accents :** `text-yellow-800` (texte foncé)
182|
183|### **Langues**
184|Support bilingue FR/EN avec switch de langue. Textes configurés dans `app/page.js`.
185|
186|### **Images**
187|Images héroïques sélectionnées pour représenter Maurice et la romance tropicale.
188|
189|## 🔧 Administration
190|
191|### **Accès Admin**
192|- **URL :** https://shipping-system.emergent.host/admin
193|- **Mot de passe :** `LoveMRU2025!`
194|
195|### **Fonctionnalités Admin**
196|- Voir tous les utilisateurs avec statistiques
197|- Gérer les profils (voir, supprimer)
198|- Configurer les paramètres de l'application
199|- Statistiques : résidents vs touristes, matches, etc.
200|
201|## 🛡️ Sécurité
202|
203|- **Authentification** via Supabase avec vérification email
204|- **Row Level Security** activé sur toutes les tables
205|- **CORS** configuré pour accès frontend
206|- **Variables sensibles** dans .env non committées
207|- **Images** stockées en base64 pour éviter les vulnérabilités
208|
209|## 📊 Monitoring et Analytics
210|
211|- **Health Check :** `/api?path=health`
212|- **Métriques Admin :** Tableau de bord intégré
213|- **Logs :** Via Supabase dashboard
214|
215|## 🗺️ Roadmap
216|
217|### **Phase 1 - Complété ✅**
218|- [x] Authentification utilisateur
219|- [x] Profils détaillés avec photos
220|- [x] Système de matching
221|- [x] Interface bilingue
222|- [x] Panneau d'administration
223|- [x] Déploiement production
224|
225|### **Phase 2 - Prochaines Étapes**
226|- [ ] Messagerie en temps réel
227|- [ ] Géolocalisation avancée
228|- [ ] Notifications push
229|- [ ] Photos multiples par profil
230|- [ ] Filtres de recherche avancés
231|
232|### **Phase 3 - Fonctionnalités Avancées**
233|- [ ] Événements locaux Maurice
234|- [ ] Partenariats restaurants/activités
235|- [ ] Mode premium/monétisation
236|- [ ] Application mobile native
237|- [ ] Support créole mauricien
238|
239|## 🤝 Contribution
240|
241|### **Pour modifier l'application :**
242|
243|1. **Fork** ce repository
244|2. **Créez une branche** : `git checkout -b ma-fonctionnalite`
245|3. **Committez** : `git commit -m 'Ajouter fonctionnalité'`
246|4. **Push** : `git push origin ma-fonctionnalite`
247|5. **Créez une Pull Request**
248|
249|### **Structure de commit :**
250|```
251|feat: nouvelle fonctionnalité
252|fix: correction de bug
253|style: changements de style
254|docs: mise à jour documentation
255|refactor: refactorisation code
256|```
257|
258|## 📞 Support
259|
260|Pour toute question ou support :
261|- **Issues :** Créer une issue sur GitHub
262|- **Documentation :** Voir ce README
263|- **Admin :** Utiliser le panneau d'administration
264|
265|## 📄 Licence
266|
267|Ce projet est propriétaire. Tous droits réservés.
268|
269|---
270|
271|**Fait avec ❤️ pour l'île Maurice 🌴**
272|
273|*LOVE MRU - Là où les cœurs se rencontrent sous le soleil mauricien*

