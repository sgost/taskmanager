<template>
  <div id="table_main">
    <div id="table_main_container">
      <div id="menu">
        <div id="menu_b1">
          <img src="../assets/hotKup.svg" id="img1" />
          <img src="../assets/hamburger.svg" id="img2" />
        </div>
        <div id="menu_b2">
          <p>
            <img src="../assets/tick2.svg" id="img1" /><img
              src="../assets/tick1.svg"
              id="img2"
            />TASKS
          </p>
          <p>
            <img src="../assets/cal2.svg" id="img1" />
            <img src="../assets/cal1.svg" id="img2" />CALENDAR
          </p>
          <p>
            <img src="../assets/chann2.svg" id="img1" />
            <img src="../assets/chann1.svg" id="img2" />CHANNELS
          </p>
          <p>
            <img src="../assets/chat2.svg" id="img1" />
            <img src="../assets/chat1.svg" id="img2" />CHAT
          </p>
          <p>
            <img src="../assets/repo2.svg" id="img1" />
            <img src="../assets/repo1.svg" id="img2" />REPORTS
          </p>
          <p>
            <img src="../assets/dash2.svg" id="img1" />
            <img src="../assets/dash1.svg" id="img2" />DASHBOARDS
          </p>
        </div>
        <div id="menu_b3">
          <p><img src="../assets/settings.svg" id="img1" />SETTINGS</p>
        </div>
      </div>

      <div id="menu_container">
        <div id="search_container">
          <div id="search_bar">
            <img src="../assets/search.svg" />
            <input type="search" placeholder="search" />
          </div>
          <div id="button">
            <button id="btn1">
              <img src="../assets/pencil.svg" />New Task
            </button>
            <button id="btn2"></button>
          </div>
          <div id="profile">
            <img src="../assets/notification.svg" id="notification" />
            <img src="../assets/avatar.svg" id="avatar" />
            <p>Pavan B</p>
          </div>
        </div>

        <div id="inbox_container">
          <div id="ind_top">
            <button>
              Inbox<span>(18)</span
              ><img src="../assets/drop_black.svg" id="drop" />
            </button>
            <button><img src="../assets/Filter.svg" /></button>
          </div>
          <div id="ind_middle">
            <div id="cards">
              <div id="card_top">
                <button>MAINTENANCE</button>
                <button>...</button>
              </div>
              <div id="card_middle">
                <p>
                  Please fix my computer network connection. Both LAN and Wi-Fi
                  are not working
                </p>
                <p><span>#</span>Task ID: 1476</p>
              </div>
              <div id="card_bottom">
                <div id="profile">
                  <img src="../assets/avatar.svg" id="avatar" />
                  <p>Pavan B</p>
                </div>
                <button>
                  <img src="../assets/clock.svg" id="clock" />07 AUG
                </button>
              </div>
            </div>
            <div id="cards">
              <div id="card_top">
                <button>MAINTENANCE</button>
                <button>...</button>
              </div>
              <div id="card_middle">
                <p>
                  Please fix my computer network connection. Both LAN and Wi-Fi
                  are not working
                </p>
                <p><span>#</span>Task ID: 1476</p>
              </div>
              <div id="card_bottom">
                <div id="profile">
                  <img src="../assets/avatar.svg" id="avatar" />
                  <p>Pavan B</p>
                </div>
                <button>
                  <img src="../assets/clock.svg" id="clock" />07 AUG
                </button>
              </div>
            </div>

            <div id="cards">
              <div id="card_top">
                <button>MAINTENANCE</button>
                <button>...</button>
              </div>
              <div id="card_middle">
                <p>
                  Please fix my computer network connection. Both LAN and Wi-Fi
                  are not working
                </p>
                <p><span>#</span>Task ID: 1476</p>
              </div>
              <div id="card_bottom">
                <div id="profile">
                  <img src="../assets/avatar.svg" id="avatar" />
                  <p>Pavan B</p>
                </div>
                <button>
                  <img src="../assets/clock.svg" id="clock" />07 AUG
                </button>
              </div>
            </div>
          </div>
        </div>
        <div id="inbox_container2">
          <h1>hi</h1>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Table",
};
</script>

<style scoped>
#table_main {
  padding: 24px;
}
#table_main_container {
  display: flex;
}
#menu {
  width: fit-content;
  height: fit-content;
  background: #ffffff;
  box-shadow: 0px 0px 12px rgba(16, 38, 73, 0.06);
  border-radius: 17.9778px;
  padding: 10px 0px 32px;
}
#menu #menu_b1 {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
}
#menu #menu_b1 #img1 {
  width: 108px;
  height: 26px;
}
#menu #menu_b1 #img2 {
  width: 32px;
  height: 32px;
  margin-left: 48px;
  cursor: pointer;
}
#menu #menu_b2 {
  margin: 48px 0 0 0;
  width: 100%;
}
#menu #menu_b2 p {
  padding: 16px 0 16px 14px;
  font-style: normal;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
  display: flex;
  align-items: center;
  color: #65676d;
  cursor: pointer;
  transition: 0.5s ease-in-out;
}
#menu #menu_b2 p img {
  width: 24px;
  height: 24px;
  margin: 0 10px 0 0;
}
#menu #menu_b2 p #img2 {
  display: none;
}
#menu #menu_b2 p:hover {
  background: #e6f2ff;
  color: #0077d7;
  border-right: 6px solid #0077d7;
}
#menu #menu_b2 p:hover #img1 {
  display: none;
}
#menu #menu_b2 p:hover #img2 {
  display: block;
}
#menu #menu_b3 {
  margin: 200px 0 0 0;
}
#menu #menu_b3 p {
  padding: 0 0 0 14px;
  font-style: normal;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
  display: flex;
  align-items: center;
  color: #65676d;
  cursor: pointer;
  transition: 0.5s ease-in-out;
}
#menu #menu_b3 p img {
  width: 24px;
  height: 24px;
  margin: 0 10px 0 0;
}

#menu_container {
  width: 85%;
  height: 100%;
  margin-left: 24px;
  display: grid;
  gap: 22px;
  grid-template-columns: auto auto auto;
}
#menu_container #search_container {
  background: #ffffff;
  box-shadow: 0px 0px 12px rgba(16, 38, 73, 0.06);
  border-radius: 8px;
  display: flex;
  align-items: center;
  padding: 9px 16px;
  grid-column: 1/4;
  grid-row: 1;
}
#menu_container #search_container #search_bar {
  padding: 2px 96.1539px 2px 15.3846px;
  width: 28%;
  background: #f7f6f4;
  border-radius: 8px;
  height: 56px;
  position: relative;
  display: flex;
  align-items: center;
  height: 40px;
}
#menu_container #search_container #search_bar input {
  width: 100%;
  height: 100%;
  font-weight: 500;
  font-size: 13.8px;
  background: transparent;
  border: none;
  outline: none;
  padding: 7px 0 7px 12px;
}
#menu_container #search_container #search_bar img {
  width: 18.4px;
  height: 18.4px;
  margin: auto;
}
#menu_container #button {
  display: flex;
  background: #0077d7;
  border-radius: 4px;
  margin: auto 0 auto 270px;
}
#menu_container #button button {
  background: transparent;
  outline: none;
  border: none;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 22px;
  color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}
#menu_container #button #btn1 {
  width: 140px;
  height: 40px;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 22px;
  color: #ffffff;
  justify-content: left;
}
#menu_container #button #btn1 img {
  margin: 0 10px 0 12px;
}
#menu_container #button #btn2 {
  width: 30px;
  height: 40px;
  border-left: 1px solid white;
}
#menu_container #profile {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto 0 auto auto;
}
#menu_container #profile #notification {
  width: 24px;
  height: 24px;
  margin: 0 22px 0 0;
  cursor: pointer;
}
#menu_container #profile #avatar {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  border: 2px solid #0077d7;
  cursor: pointer;
}
#menu_container #profile p {
  margin: 0 5px;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  color: #000000;
  cursor: pointer;
}
#menu_container #inbox_container {
  width: 354px;
}
#menu_container #inbox_container #ind_top {
  display: flex;
  justify-content: space-between;
}
#menu_container #inbox_container #ind_top button {
  display: flex;
  justify-content: center;
  align-items: center;
  background: #ffffff;
  border: 0.5px solid #aaaaaa;
  box-sizing: border-box;
  border-radius: 4px;
  width: 119px;
  height: 36px;
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 17px;
  cursor: pointer;
}
#menu_container #inbox_container #ind_top button span {
  font-weight: 200;
}
#menu_container #inbox_container #ind_top button #drop {
  margin-left: 30px;
}
#menu_container #inbox_container #ind_top button:nth-child(2) {
  width: 36px;
  height: 36px;
}
#menu_container #inbox_container #ind_middle {
  display: grid;
  grid-template-columns: 100%;
  gap: 18px;
  margin: 18px 0 0 0;
}
#menu_container #inbox_container #ind_middle #cards {
  background: #ffffff;
  box-shadow: 0px 0px 12px rgba(16, 38, 73, 0.06);
  border-radius: 8px;
  height: 141px;
  padding: 16px;
  transition: 0.5s ease-in-out;
}
#menu_container #inbox_container #ind_middle #cards:hover {
  border: 2px solid #0077d7;
  box-shadow: 0px 0px 20px rgba(18, 73, 164, 0.2);
}
#menu_container #inbox_container #ind_middle #cards #card_top {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
#menu_container #inbox_container #ind_middle #cards #card_top button {
  padding: 6px 8px;
  border: none;
  outline: none;
  font-style: normal;
  font-weight: 600;
  font-size: 10px;
  cursor: pointer;
  border-radius: 4px;
}
#menu_container
  #inbox_container
  #ind_middle
  #cards
  #card_top
  button:nth-child(2) {
  background: transparent;
  cursor: pointer;
  padding: 0;
  font-size: 15px;
}
#menu_container #inbox_container #ind_middle #cards #card_middle p {
  width: 322px;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  color: #200e32;
  margin-top: 10px;
}
#menu_container
  #inbox_container
  #ind_middle
  #cards
  #card_middle
  p:nth-child(2) {
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 15px;
  color: #200e32;
}
#menu_container
  #inbox_container
  #ind_middle
  #cards
  #card_middle
  p:nth-child(2)
  span {
  border: 1px solid #200e32;
  padding: 1.5px 6px;
  border-radius: 3px;
  margin: 0 5px 0 0;
  font-weight: 600;
}
#menu_container #inbox_container #ind_middle #cards #card_bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 10px 0 0 0;
}
#menu_container #inbox_container #ind_middle #cards #card_bottom #profile {
  display: flex;
  align-items: center;
  width: fit-content;
  margin: 0;
}
#menu_container
  #inbox_container
  #ind_middle
  #cards
  #card_bottom
  #profile
  #avatar {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  border: 0.7px solid #0077d7;
  cursor: pointer;
}
#menu_container #inbox_container #ind_middle #cards #card_bottom #profile p {
  margin: 0 5px;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  color: #000000;
  cursor: pointer;
}
#menu_container #inbox_container #ind_middle #cards #card_bottom button {
  padding: 1.93667px 7.74669px;
  border: none;
  outline: none;
  cursor: pointer;
  border-radius: 4px;
  color: white;
  font-style: normal;
  font-weight: 500;
  font-size: 10px;
  line-height: 15px;
  display: flex;
  align-items: center;
  color: #ffffff;
  background: #16c45f;
}
#menu_container #inbox_container #ind_middle #cards #card_bottom button #clock {
  margin: 0 7px 0 0;
  width: 10px;
  height: 10px;
}
#menu_container #inbox_container2 {
  border: 1px solid yellow;
  width: 700px;
}
</style>