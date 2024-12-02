1. Mettre en place l'exemple d'application React
Si vous avez déjà un exemple d'application React qui vous a été fourni, vous pouvez commencer par l'installer et le configurer.
Sinon, créez une application React simple avec plusieurs composants ayant de l'état local (via useState) et des accessoires (via props). Vous pouvez utiliser Create React App pour démarrer rapidement :
bash
Copier le code
npx create-react-app my-debugging-app
cd my-debugging-app
npm start
2. Installer l'extension React Developer Tools
Si vous n'avez pas encore installé React Developer Tools, vous pouvez le faire en ajoutant l'extension à votre navigateur.
Chrome : Allez sur React Developer Tools sur Chrome Web Store.
Firefox : Allez sur React Developer Tools sur Firefox Add-ons.
Une fois installée, redémarrez votre navigateur pour activer l'extension.
3. Inspecter l'arbre des composants
Ouvrez l'application React dans votre navigateur.
Ouvrez les outils de développement de votre navigateur (F12 ou Ctrl + Shift + I).
Cliquez sur l'onglet React pour accéder à React Developer Tools.
Vous pourrez voir l'arbre des composants de votre application sous forme hiérarchique. Cliquez sur chaque composant pour inspecter ses propriétés (props) et son état (state).
4. Identifier les problèmes
Recherchez les problèmes suivants dans l'application :

État incorrect : Vérifiez si les valeurs de l'état ne correspondent pas à ce que vous attendiez. Par exemple, un composant peut avoir un état qui ne change pas comme prévu.
Accessoires manquants : Vérifiez si certains composants reçoivent les accessoires attendus. Si un composant dépend d'un prop qui n'est pas transmis correctement, cela pourrait entraîner un comportement inattendu.
Comportement inattendu : Si un composant ne se met pas à jour correctement ou ne réagit pas comme prévu (par exemple, un bouton ne change pas de couleur après un clic), cela peut être dû à un problème avec l'état ou les props.
5. Utiliser React Developer Tools pour diagnostiquer les problèmes
Voici quelques outils clés dans React Developer Tools qui vous aideront à diagnostiquer et corriger les problèmes :

Inspecter l'état d'un composant : Cliquez sur un composant dans l'arbre pour voir son état. Si vous voyez une valeur incorrecte, vous pouvez l'ajuster manuellement pour tester si le problème vient de là.
Inspecter les props : Vérifiez que les accessoires passés au composant sont bien ceux attendus. S'il manque des props, cela pourrait expliquer un comportement inattendu.
Profiler : Le panneau Profiler permet de voir la performance de votre application et de diagnostiquer les rendus inutiles ou trop fréquents des composants. Cela peut vous aider à repérer les problèmes de performance.
6. Diagnostiquer les erreurs dans l'application
Si des erreurs apparaissent dans la console (erreurs React, erreurs JavaScript), lisez-les attentivement pour comprendre la source du problème.
Par exemple, un message comme "Failed prop type" peut indiquer qu'un prop n'a pas le type attendu.
Utilisez l'outil React Developer Tools pour vérifier les types des props et assurez-vous qu'ils sont corrects.
7. Corriger les problèmes
Après avoir identifié les problèmes, appliquez les corrections nécessaires. Voici quelques exemples de problèmes courants et leurs solutions :

Problème de mise à jour de l'état : Si l'état ne se met pas à jour correctement, assurez-vous que vous utilisez correctement useState ou setState pour modifier l'état. Parfois, des erreurs peuvent survenir si vous mettez à jour l'état de manière incorrecte, par exemple en essayant de modifier directement un objet ou un tableau au lieu de créer une nouvelle copie.
Problème de props manquants ou incorrects : Si un prop est manquant ou incorrect, assurez-vous qu'il est bien passé depuis le composant parent. Utilisez prop-types pour ajouter des vérifications de type aux props afin de faciliter le débogage.
8. Documenter le processus de débogage
Une fois les problèmes identifiés et corrigés, documentez le processus de débogage. Voici ce que vous pourriez inclure :

Description des problèmes : Décrivez les problèmes identifiés dans l'application.
Diagnostic : Expliquez comment vous avez utilisé React Developer Tools pour identifier ces problèmes.
Solutions mises en œuvre : Expliquez les modifications que vous avez apportées pour résoudre les problèmes (par exemple, corriger l'état, ajouter des props, refactoriser un composant, etc.).
9. Vérification après débogage
Testez votre application pour vous assurer que les problèmes ont été résolus.
Vérifiez que l'état se met à jour correctement, que les props sont bien transmis, et que les composants réagissent comme prévu.
Exemple de Débogage avec React Developer Tools :
Imaginons que vous avez un composant Counter qui affiche un compteur et un bouton pour l'incrémenter. Le compteur ne s'incrémente pas correctement. Vous pouvez inspecter l'état du composant dans React Developer Tools pour vérifier si la valeur du compteur est bien modifiée à chaque clic. Si vous constatez que l'état n'est pas mis à jour, vous pouvez corriger l'utilisation de setState ou useState.

En suivant ces étapes, vous devriez être en mesure d'identifier et de corriger les problèmes rencontrés dans l'exemple d'application React.