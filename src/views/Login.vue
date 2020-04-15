<template>
  <!-- FORMULAIRE -->
  <div class="container-fluid body p-5">
    <h1
      class="phrase font-weight-bold text-center"
    >Vous souhaitez prendre contact avec moi, merci de remplir ce formulaire. A bientôt !</h1>

    <form id="myForm">
      <span class="form_col">Sexe:</span>
      <label>
        <input name="sex" type="radio" value="H" />Homme
      </label>
      <label>
        <input name="sex" type="radio" value="F" />Femme
      </label>
      <span class="erreur">Vous devez sélectionnez votre sexe</span>
      <br />
      <br />

      <label class="form_col" for="lastName">Nom:</label>
      <input name="lastName" id="lastName" type="text" />
      <span class="erreur">Un nom ne peut pas faire moins de 2 caractères</span>
      <br />
      <br />

      <label class="form_col" for="firstName">Prénom:</label>
      <input name="firstName" id="firstName" type="text" />
      <span class="erreur">Un prénom ne peut pas faire moins de 2 caractères</span>
      <br />
      <br />

      <label class="form_col" for="age">Âge:</label>
      <input name="age" id="age" type="text" />
      <span class="erreur">L'âge doit être compris entre 5 et 140</span>
      <br />
      <br />

      <label class="form_col" for="login">Pseudo:</label>
      <input name="login" id="login" type="text" />
      <span class="erreur">Le pseudo ne peut pas faire moins de 4 caractères</span>
      <br />
      <br />

      <label class="form_col" for="login">Email:</label>
      <input name="email" id="email" type="text" />
      <span
        class="erreur"
      >L'adresse mail doit contenir un nom d'utilisateur, le caractère @ et un nom de domaine</span>
      <br />
      <br />

      <label class="form_col" for="pwd1">Mot de passe:</label>
      <input name="pwd1" id="pwd1" type="password" />
      <span class="erreur">Le mot de passe ne doit pas faire moins de 6 caractères</span>
      <br />
      <br />

      <label class="form_col MDP" for="pwd2">Mot de passe (confirmation):</label>
      <label class="form_col d-lg-none" for="pwd2">Confirmer MDP:</label>
      <input name="pwd2" id="pwd2" type="password" />
      <span class="erreur">Le mot de passe de confirmation doit être identique à celui d'origine</span>
      <br />
      <br />

      <label class="form_col" for="country">Pays :</label>
      <select name="country" id="country">
        <option value="none">Sélectionnez votre pays de résidence</option>
        <option value="en">Angleterre</option>
        <option value="us">États-Unis</option>
        <option value="fr">France</option>
      </select>
      <span class="erreur">Vous devez sélectionner votre pays de résidence</span>
      <br />
      <br />

      <span class="form_col"></span>
      <label>
        <input name="news" type="checkbox" /> Je désire recevoir la newsletter chaque mois.
      </label>
      <br />
      <br />

      <span class="form_col"></span>
      <input type="submit" value="M'inscrire" />
      <input type="reset" value="Réinitialiser le formulaire" />
    </form>
  </div>
</template>
<script>
export default {};

// Fonction de désactivation de l'affichage des "tooltips"
function deactivateTooltips() {
  var tooltips = document.querySelectorAll(".erreur"),
    tooltipsLength = tooltips.length;

  for (var i = 0; i < tooltipsLength; i++) {
    tooltips[i].style.display = "none";
  }
}

// La fonction ci-dessous permet de récupérer la "tooltip" qui correspond à notre input

function getTooltip(elements) {
  while ((elements = elements.nextSibling)) {
    if (elements.className === "erreur") {
      return elements;
    }
  }
  return false;
}

// Fonctions de vérification du formulaire, elles renvoient "true" si tout est ok
var check = {}; // On met toutes nos fonctions dans un objet littéral

check["sex"] = function() {
  var sex = document.getElementsByName("sex"),
    tooltipStyle = getTooltip(sex[1].parentNode).style;

  if (sex[0].checked || sex[1].checked) {
    tooltipStyle.display = "none";
    return true;
  } else {
    tooltipStyle.display = "inline-block";
    return false;
  }
};

check["lastName"] = function(id) {
  var name = document.getElementById(id),
    tooltipStyle = getTooltip(name).style;

  if (name.value.length >= 2) {
    name.className = "correct";
    tooltipStyle.display = "none";
    return true;
  } else {
    name.className = "incorrect";
    tooltipStyle.display = "inline-block";
    return false;
  }
};

check["firstName"] = check["lastName"]; // La fonction pour le prénom est la même que celle du nom

check["age"] = function() {
  var age = document.getElementById("age"),
    tooltipStyle = getTooltip(age).style,
    ageValue = parseInt(age.value);

  if (!isNaN(ageValue) && ageValue >= 5 && ageValue <= 140) {
    age.className = "correct";
    tooltipStyle.display = "none";
    return true;
  } else {
    age.className = "incorrect";
    tooltipStyle.display = "inline-block";
    return false;
  }
};

check["login"] = function() {
  var login = document.getElementById("login"),
    tooltipStyle = getTooltip(login).style;

  if (login.value.length >= 4) {
    login.className = "correct";
    tooltipStyle.display = "none";
    return true;
  } else {
    login.className = "incorrect";
    tooltipStyle.display = "inline-block";
    return false;
  }
};

check["email"] = function() {
  var email = document.getElementById("email"),
    tooltipStyle = getTooltip(email).style;

  var pattern = /^[a-z0-9\-_\.]+@[a-z0-9]+\.[a-z]{2,5}$/;
  if (email.value.match(pattern)) {
    email.className = "correct";
    tooltipStyle.display = "none";
    return true;
  } else {
    email.className = "incorrect";
    tooltipStyle.display = "inline-block";
    return false;
  }
};

check["pwd1"] = function() {
  var pwd1 = document.getElementById("pwd1"),
    tooltipStyle = getTooltip(pwd1).style;

  if (pwd1.value.length >= 6) {
    pwd1.className = "correct";
    tooltipStyle.display = "none";
    return true;
  } else {
    pwd1.className = "incorrect";
    tooltipStyle.display = "inline-block";
    return false;
  }
};

check["pwd2"] = function() {
  var pwd1 = document.getElementById("pwd1"),
    pwd2 = document.getElementById("pwd2"),
    tooltipStyle = getTooltip(pwd2).style;

  if (pwd1.value == pwd2.value && pwd2.value != "") {
    pwd2.className = "correct";
    tooltipStyle.display = "none";
    return true;
  } else {
    pwd2.className = "incorrect";
    tooltipStyle.display = "inline-block";
    return false;
  }
};

check["country"] = function() {
  var country = document.getElementById("country"),
    tooltipStyle = getTooltip(country).style;

  if (country.options[country.selectedIndex].value != "none") {
    tooltipStyle.display = "none";
    return true;
  } else {
    tooltipStyle.display = "inline-block";
    return false;
  }
};

// Mise en place des événements
(function() {
  // Utilisation d'une IIFE pour éviter les variables globales.

  var myForm = document.getElementById("myForm"),
    inputs = document.querySelectorAll(
      "input[type=text], input[type=password]"
    ),
    inputsLength = inputs.length;

  for (var i = 0; i < inputsLength; i++) {
    inputs[i].addEventListener("keyup", function(e) {
      check[e.target.id](e.target.id); // "e.target" représente l'input actuellement modifié
    });
  }

  myForm.addEventListener("submit", function(e) {
    var result = true;

    for (var i in check) {
      result = check[i](i) && result;
    }
    if (result) {
      alert("Le formulaire est bien rempli.");
    }
    e.preventDefault();
  });

  myForm.addEventListener("reset", function() {
    for (var i = 0; i < inputsLength; i++) {
      inputs[i].className = "";
    }
    deactivateTooltips();
  });
})();

// Maintenant que tout est initialisé, on peut désactiver les "tooltips"
deactivateTooltips();
</script>
<style>
</style>
