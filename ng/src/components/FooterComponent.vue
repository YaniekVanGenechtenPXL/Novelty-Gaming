<template>
  <footer>
    <div id="logoContainer">
      <img id="img_logoExt" src="../assets/logos/Logo_White_Ext.png" alt="Logo" />
      <img id="img_logoMin" src="../assets/logos/Logo_White.png" alt="Logo" />
    </div>
    <div id="contact">
      <h3>Contact</h3>
      <form @submit.prevent="">
        <input name="email" id="email" type="email" placeholder="Email" >
        <textarea name="message" id="message" placeholder="Type your message"></textarea>
        <div id="footer__form__buttons">
          <button type="submit" class="buttonPrimary">Submit</button>
          <button class="buttonSecondary" type="reset">Reset</button>
        </div>
      </form>
    </div>
    <div id="otherPages">
      <h3>Other pages</h3>
      <ul>
        <li>
          <router-link to="/">Keycaps</router-link>
        </li>
        <li>
          <router-link to="/">Keyboards</router-link>
        </li>
        <li>
          <router-link to="/">Mousepads</router-link>
        </li>
        <li>
          <router-link to="/">Cables</router-link>
        </li>
        <li>
          <router-link to="/">About us</router-link>
        </li>
      </ul>
    </div>
    <div id="follow">
      <h3>Follow us</h3>
      <div id="imgContainer">
        <a href="#" target="_blank">
          <img src="../assets/icons/youtube.png" alt="YouTube" />
        </a>
        <a href="https://www.instagram.com/noveltygamings?igsh=N2JlMHNubjVxenFq" target="_blank">
          <img src="../assets/icons/instagram.png" alt="Instagram" />
        </a>
        <a href="#" target="_blank">
          <img src="../assets/icons/facebook.png" alt="Facebook" />
        </a>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  background-color: var(--black);
  width: 100vw;
  padding: 30px 10vw;
  display: flex;
  justify-content: space-between;
  color: var(--white);
  img#img_logoMin {
    display: none;
  }
  div#logoContainer {
    img {
      height: 70px;
    }
  }
  div#contact {
    form {
      display: flex;
      flex-direction: column;
      input {
        width: 15vw;
        border-radius: 5px;
        border: none;
        padding: 5px;
        margin-bottom: 5px;
      }
      textarea {
        width: 15vw;
        height: 8vh;
        border-radius: 5px;
        border: none;
        padding: 5px;
        resize: none;
      }
      div#footer__form__buttons {
        width: 100%;
        display: flex;
        justify-content: space-between;
        margin-top: 10px;
        button {
          width: 45%;
          border: none;
          border-radius: 5px;
          padding: 5px;
          cursor: pointer;
          &.buttonPrimary {
            background-color: var(--white);
            color: var(--black);
          }
          &.buttonSecondary {
            background-color: var(--black);
            border: 2px solid var(--white);
            color: var(--white);
          }
        }
      }
    }
  }
  div#otherPages {
    ul {
      display: flex;
      flex-direction: column;
      gap: 5px;
      li {
      list-style: none;
      a {
        text-decoration: none;
        color: var(--white);
      }
      &:hover {
        text-decoration: underline;
      }
    }
    }
  }
  div#follow {
    div#imgContainer {
      min-width: 220px;
      display: flex;
      justify-content: space-between;
      gap: 50px;
      margin-top: 20px;
      position: relative;
      a {
        img {
          height: 40px;
        }
      }
    }
  }
}

@media (max-width: 1220px) {
  footer {
    img#img_logoExt {
      display: none;
    }
    img#img_logoMin {
      display: block;
    }
  }
}

@media (min-width: 600px) and (max-width: 1100px) {
  footer {
    flex-direction: row;
    flex-wrap: wrap;
    div {
      margin-bottom: 50px;
    }
    div#contact {
      width: 100%;
      form {
        input {
          width: 100%;
        }
        textarea {
          width: 100%;
          height: 15vh;
        }
      }
    }
    div#otherPages {
      width: 50%;
    }
    div#follow {
      width: 50%;
    }
  }
}

@media (max-width: 600px) {
  footer {
    flex-direction: row;
    flex-wrap: wrap;
    div {
      margin-bottom: 50px;
    }
    div#contact {
      width: 100%;
      form {
        input {
          width: 100%;
        }
        textarea {
          width: 100%;
          height: 15vh;
        }
      }
    }
    div#otherPages {
      width: 100%;
    }
    div#follow {
      width: 100%;
    }
  }
}
</style>