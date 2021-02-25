<template>
  <div>
    <div class="flex justify-center">
      <div class="logo inline-block">
        <a @click="$router.push('/')"><img src="..\assets\logo.jpg" /></a>
      </div>
      <div id="main_menu" class="w-2/3 inline-block my-auto">
        <ul>
          <li><a @click="$router.push('/')">トップ</a></li>
          <li><a @click="$router.push('/access')">アクセス</a></li>
          <li><a @click="$router.push('/faq')">Q＆A</a></li>
          <li><a @click="$router.push('/links')">リンク集</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>
<style scoped>
.logo {
  width: 15%;
}
#main_menu ul {
  display: flex;
  margin: 0 auto;
  padding: 0;
  text-align: center;
}
#main_menu li {
  display: inline-block;
  width: calc(100% / 4);
  font-size: 1.1vw;
}
#main_menu a {
  display: block;
  width: 100%;
  padding: 0.5rem;
  color: #555;
}
#main_menu a:hover {
  color: #ce5242;
}

#nav-drawer {
  /* 場所を固定 */
  position: fixed;
}

/*チェックボックス等は非表示に*/
.nav-unshown {
  display: none;
}

/*アイコンのスペース*/
#nav-open {
  display: inline-block;
  width: calc(100vw / 10);
  height: calc(5vh / 10);
}

/*ハンバーガーアイコンをCSSだけで表現*/
#nav-open span,
#nav-open span:before,
#nav-open span:after {
  position: relative;
  height: 1px; /*線の太さ*/
  width: 25px; /*長さ*/
  border-radius: 1px;
  background: #4b4b4b;
  display: block;
  content: '';
  cursor: pointer;
}
#nav-open span:before {
  bottom: -8px;
}
#nav-open span:after {
  bottom: -16px;
}

/*閉じる用の薄黒カバー*/
#nav-close {
  display: none; /*はじめは隠しておく*/
  position: fixed;
  z-index: 99;
  top: 0; /*全体に広がるように*/
  left: 0;
  width: 100%;
  height: 100%;
  background: black;
  opacity: 0;
  transition: 0.3s ease-in-out;
}

/*中身*/
#nav-content {
  color: #1a1c21;
  font-family: 'YuGothic';
  font-weight: bold;
  overflow: auto;
  position: fixed;
  text-align: left;
  top: 0;
  left: 0;
  z-index: 9999; /*最前面に*/
  width: 90%; /*右側に隙間を作る（閉じるカバーを表示）*/
  max-width: 330px; /*最大幅（調整してください）*/
  height: 100%;
  padding: 1rem;
  background: #fffffc; /*背景色*/
  transition: 0.3s ease-in-out; /*滑らかに表示*/
  -webkit-transform: translateX(-105%);
  transform: translateX(-105%); /*左に隠しておく*/
}

#nav-content a::before {
  background: url('../assets/arrow.svg') no-repeat;
  content: '';
  display: inline-block;
  height: 1.25em;
  margin-right: 1.25em;
  position: relative;
  top: 3px;
  width: 1.25em;
}

#nav-content li::after {
  content: '';
  display: block;
  width: 100%;
  height: 1px;
  background-color: #4b4b4b;
  position: relative;
  top: 0.5rem;
}
/*チェックが入ったらもろもろ表示*/
#nav-input:checked ~ #nav-close {
  display: block; /*カバーを表示*/
  opacity: 0.5;
}

#nav-input:checked ~ #nav-content {
  -webkit-transform: translateX(0%);
  transform: translateX(0%); /*中身を表示（右へスライド）*/
  box-shadow: 6px 0 25px rgba(0, 0, 0, 0.15);
}
</style>
