Creation de project avec `ng new TrelloCorrection`

hide les files derengeantes : https://marketplace.visualstudio.com/items?itemName=roonie007.hide-files

Project doit etre organiser comme ceci :

```
	/app
		/components
		/models
		/services
```

l'extention Angular me permet d'avoir des icones propres a Angulars

---

Creer les components necessaires :

` ng generate components 'nom'`
ou
`ng g c 'nom'`

ainsi le dossier devra etre defini avant le nom

-> `ng g c components/nom`
-> `ng g s Service/nom`

---

Une fois mon architecture bonne et mes Composents generer je peux commencer a coder

Pour afficher un composant dans un autre composant il faut l'importer dans le fichier ts du composant parent

Une fois le composant importée il peut etre utiliser dans l'html du composant parent

afficher les composents qui nous interressent.

---

Pour afficher de l'information dynamique, Je vais devoir ajouter ces data dans mon fichier ts.

Partager les data entre les composents :

@Input() permet de passer des data d'un composant parent a un composant enfant

Voici comment l'utiliser :

```html
// Dans le composant parent
<app-child [data]="data"></app-child>

// Dans le composant enfant @Input() data: any;
```

Description

    La directive ngFor est utilisée pour itérer sur une collection de données et afficher une liste d'éléments dans le DOM.

Syntaxe de Base

angular

\*ngFor="let item of items; let i = index; let odd = odd; let even = even; let first = first; let last = last; trackBy: trackByFn"

Paramètres

    item: L'élément actuel dans la collection.
    items: La collection de données à itérer.
    index: L'index de l'élément actuel dans la collection.

Exemples
Itération Simple

```typescript
<div *ngFor="let item of items">{{item}}</div>
```

Accès à l'Index

```typescript
<div *ngFor="let item of items; let i = index">{{i}} - {{item}}</div>
```
