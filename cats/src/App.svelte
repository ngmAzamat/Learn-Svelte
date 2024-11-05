<script>
  let isActive = false;
  function toggleMenu() {
    isActive = !isActive;
  }
</script>
<style>
  * {
    color: black;
  }
  a {
  color: aqua;
  text-decoration: none;
}

.open {
  display: flex !important;
}

.nav ul {
  display: flex;
  width: 100%;
  justify-content: space-between;
  list-style: none;
}
.burger {
  display: flex;
  position: relative;
  z-index: 50;
  justify-content: flex-end;
  width: 30px;
  height: 18px;
}
.burger span {
  height: 2px;
  width: 100%;
  color: #000;
  transform: scale(1);
}

.burger::before,
.burger::after {
  position: absolute;
  content: "";
  height: 2px;
  width: 100%;
  background-color: #003cff;
  transition: all 0.3s ease 0s;
}

.burger::before {
  top: 0;
}
.burger::after {
  bottom: 0;
}
.burger.active span {
  transform: scale(0);
}

.burger.active::before {
  top: 50%;
  transform: rotate(-45deg) translate(0, -50%);
}
.burger.active::after {
  bottom: 50%;
  transform: rotate(45deg) translate(0, 50%);
}

@media (max-width: 2000px) {
  .burger {
    display: none;
  }
  .nav {
    display: none;
  }
}

@media (max-width: 1000px) {
  .header {
    display: none;
  }
  .burger {
    display: flex;
  }
  .nav {
    display: none;
    flex-direction: column;
    position: fixed;
    height: 100%;
    width: 100%;
    background-color: black;
    padding: 50px 40px;
    z-index: 50;
    overflow-y: auto;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    animation: BurgerAnimation 0.4s;
  }
  .nav ul {
    flex-direction: column;
    row-gap: 30px;
  }
}
@keyframes BurgerAnimation {
  from {
    opacity: o;
  }
  to {
    opacity: 1;
  }
}

.container {
  display: flex;
}
.meow {
  justify-content: center;
  align-items: center;
}
.header {
  margin: 0;
  height: 70px;
  width: 25%;
  text-align: center;
  border-bottom: 4px solid silver;
  background-color: #333;
  color: #fff;
  line-height: 70px;
}
.new {
  background-color: #333;
  color: #fafafa;
  padding: 25px;
  border: 1px solid black;
  border-collapse: collapse;
}
.main {
  width: 45%;
  margin: 5%;
  margin-top: 2.5%;
  margin-right: 2.5%;
  background-color: #fafafa;
  border: 1px solid silver;
  padding: 20px 2.5%;
  order: 1;
}
.aside {
  width: 25%;
  margin: 2.5%;
  padding: 20px 2.5%;
  background-color: #fafafa;
  border: 1px solid silver;
  order: 1;
}
.footer {
  height: 70px;
  width: 100%;
  text-align: center;
  border-bottom: 4px solid silver;
  background-color: #333;
  color: #fff;
  line-height: 70px;
}
.mount {
  height: 300px;
}

@media (min-width: 100px) and (max-width: 599px) {
  .container {
    display: grid;
    grid-template-columns: 1fr;
  }
  .header {
    margin: 0;
    height: 70px;
    width: 89%;
    text-align: center;
    border-bottom: 4px solid silver;
    background-color: #333;
    color: #fff;
    line-height: 70px;
  }
  .main {
    width: 80%;
    margin: 5%;
    margin-top: 2.5%;
    margin-right: 2.5%;
    background-color: #fafafa;
    border: 1px solid silver;
    padding: 20px 2.5%;
    order: 1;
  }
  .aside {
    width: 80%;
    margin: 2.5%;
    padding: 20px 2.5%;
    background-color: #fafafa;
    border: 1px solid silver;
    order: -1;
  }
  .mount {
    height: 250px;
  }
}

@media (min-width: 600px) and (max-width: 749px) {
    .header {
      margin: 0;
      height: 70px;
      width: 25%;
      text-align: center;
      border-bottom: 4px solid silver;
      background-color: #333;
      color: #fff;
      line-height: 70px;
    }
    .main {
      width: 45%;
      margin: 5%;
      margin-top: 2.5%;
      margin-right: 2.5%;
      background-color: #fafafa;
      border: 1px solid silver;
      padding: 1;
      order: -1;
    }
    .aside {
      width: 25%;
      margin: 1%;
      padding: 1%;
      background-color: #fafafa;
      border: 1px solid silver;
      order: 1;
    }
    .mount {
      height: 140px;

    }
}

@media (min-width: 750px) and (max-width: 999px) {
  .mount {
    height: 180px;
  }
}

@media (min-width: 1000px) and (max-width: 1450px) {
  .mount {
    height: 200px;
  }
}

</style>
<div class="container">
<div class="header"><a href="/barsik-5.svelte">Барсик V</a></div>  
<div class="header"><a href="/">a</a></div>
<div class="header"><a href="/">a</a></div>
<div class="header"></div>
    <nav class="nav" class:open={isActive}>
      <ul>
        <li><a href="/barsik-5.svelte">Барсик V</a></li>
        <li><a href="/">a</a></li>
        <li><a href="/">a</a></li>
        <li><a href="/">a</a></li>
        <li><a href="/">a</a></li>
      </ul>
    </nav>
    <div class="burger" class:active={isActive} on:click={toggleMenu}>
      <span></span>
    </div>


</div>
<div class="container">
<div class="main">
    <h3>Начало Правления</h3>
    <p>8 июля 9 года Умер Барсик III Император Всех Котов. тогда же Королем Шести Королевств стал Барсик IV.был созван совет </p>
      <p>- Хранителем государства должен стать Феликс IV и он же Лордом Мяуланна и Верховным Лордом Котического государства. - сказал Леопольд I</p>
      <p>- как минимум Север Хранить Буду Я. - Заявил Снежок V</p>
      <p>- также Родавыми Землями Востока буду владеть я. - сказал Леопольд</p>
      <p>- думую Мурсия останется за Королевой -  Заявил Снежок V</p>
      <p>- да и еще Хранителем Королевства буду тоже я. - продолжил Снежок</p>
      <p>- тут не кто не согласился - "твой Дом воевал с Императором" сказал сказал Начальник Стражи Айс I Лорд Раненн-мурра</p>
      <p>- Айсик прав. Джон Авенн станет Хранителем Королевства - сказал Барсик IV и это приказ!</p>
      <p>далее Джон Авенн просит короля подписать указ о разрешении Хранителям иметь армию так как Рекс III пересек Дюнное море и может грабить земли.</p>
      <p>Король Барсик IV  решает для верного советника титул Короля в Западном море.</p>
      <p>после этого началось Восстание Феликса IV. Король был в бешенстве он Приказал Казнить Феликса но Авенн сказал что надо идти к Раненн-мурру разбить врага.</p>
      <p>в Битве на Раненн-мурре Король в решающий моментыбл с Авенном и Он закричавь "за Императора" показал на Короля и тогда большая часть солдат перешла на сторону Короны.</p>
      <p>далее Король вернулся в Столицу и ждал когда же Мятежников побьет Авенн</p>
</div>





<div class="aside">
<table>
  <tbody>
  <tr>
    <th colspan="2">Барсик IV</th>
  </tr>
  
  <tr>
    <th colspan="2">Император Всех Котов, Король шести Королевств и Котического Королевства в частности, Лорд Авенна и Мяуланна</th>
  </tr>
  <tr>
    <th colspan="2">Рождение: 3 июля 8 года</th>

  </tr>
  <tr>
    <th colspan="2"></th>
  </tr>
  <tr>
    <th colspan="2"><img class="mount" alt="text" src="barsik-4.webp"></th>
  </tr>
  <tr>
    <th colspan="2"></th>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <th colspan="2"></th>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <th colspan="2"></th>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <th colspan="2"></th>
  </tr>
</tbody>
</table>
</div>

</div>
