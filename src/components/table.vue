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
            <button id="btn2"><img src="../assets/drop_white.svg" /></button>
          </div>
          <div id="profile">
            <img src="../assets/notification.svg" id="notification" />
            <img src="../assets/avatar.svg" id="avatar" />
            <p>Pavan B <img src="../assets/drop_black.svg" /></p>
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
          <div id="inbox_container2_top">
            <div id="prof_img">
              <img src="../assets/avatar.svg" id="avatar" />
            </div>
            <div id="prof_data">
              <p id="id">
                <span>#</span>Task ID: 1476
                <button>
                  <img src="../assets/clock.svg" id="clock" />07 AUG
                </button>
              </p>
              <p>
                Please fix my computer network connection. Both LAN and Wi-Fi
                are not working
              </p>
              <p>By Pawan Bhojanala, 12/11/2021, 5:42PM</p>
              <div id="prof_btns">
                <p>CATEGORY: <span>MAINTENANCE</span></p>
                <p>STAGE: <span>NEW</span></p>
                <p>ASSIGNEE: <span>VIGNESH BHASKAR</span></p>
              </div>
            </div>
          </div>
          <div id="inbox_container2_middle">
            <p>Description</p>
            <p>Activities</p>
            <p>Sub Taks</p>
            <p>Checklist</p>
            <p>Reminders</p>
            <p>Time Log</p>
            <p>Forms</p>
            <p>Hooks</p>
          </div>
          <div id="inbox_container2_bottom">
            <p>
              Checklist<span>(05)</span>
              <img src="../assets/plus.svg" id="plus" />
            </p>
            <p>
              01<span
                >Create Mobile Responsive Prototype for Task bench
                application</span
              ><img src="../assets/checked.svg" id="plus" />
            </p>
            <p>
              01<span
                >Create Mobile Responsive Prototype for Task bench
                application</span
              ><img src="../assets/checked.svg" id="plus" />
            </p>
          </div>
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
  padding: 1.75182481751825vw;
}
#table_main_container {
  display: flex;
}
#menu {
  width: fit-content;
  height: fit-content;
  background: #ffffff;
  box-shadow: 0 0 0.875912408759124vw rgba(16, 38, 73, 0.06);
  border-radius: 1.31224817518248vw;
  padding: 0.72992700729927vw 0 2.33576642335766vw;
}
#menu #menu_b1 {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.72992700729927vw;
}
#menu #menu_b1 #img1 {
  width: 7.88321167883212vw;
  height: 1.8978102189781vw;
}
#menu #menu_b1 #img2 {
  width: 2.33576642335766vw;
  height: 2.33576642335766vw;
  margin-left: 3.5036496350365vw;
  cursor: pointer;
}
#menu #menu_b2 {
  margin: 3.5036496350365vw 0 0 0;
  width: 100%;
}
#menu #menu_b2 p {
  padding: 1.16788321167883vw 0 1.16788321167883vw 1.02189781021898vw;
  font-style: normal;
  font-weight: 600;
  font-size: 0.875912408759124vw;
  line-height: 1.09489051094891vw;
  display: flex;
  align-items: center;
  color: #65676d;
  cursor: pointer;
  transition: 0.5s ease-in-out;
}
#menu #menu_b2 p img {
  width: 1.75182481751825vw;
  height: 1.75182481751825vw;
  margin: 0 0.72992700729927vw 0 0;
}
#menu #menu_b2 p #img2 {
  display: none;
}
#menu #menu_b2 p:hover {
  background: #e6f2ff;
  color: #0077d7;
  border-right: 0.437956204379562vw solid #0077d7;
}
#menu #menu_b2 p:hover #img1 {
  display: none;
}
#menu #menu_b2 p:hover #img2 {
  display: block;
}
#menu #menu_b3 {
  margin: 14.5985401459854vw 0 0 0;
}
#menu #menu_b3 p {
  padding: 0 0 0 1.02189781021898vw;
  font-style: normal;
  font-weight: 600;
  font-size: 0.875912408759124vw;
  line-height: 1.09489051094891vw;
  display: flex;
  align-items: center;
  color: #65676d;
  cursor: pointer;
  transition: 0.5s ease-in-out;
}
#menu #menu_b3 p img {
  width: 1.75182481751825vw;
  height: 1.75182481751825vw;
  margin: 0 0.72992700729927vw 0 0;
}

#menu_container {
  width: 85%;
  height: 100%;
  margin-left: 1.75182481751825vw;
  display: grid;
  gap: 1.60583941605839vw;
  grid-template-columns: auto auto auto auto;
}
#menu_container #search_container {
  background: #ffffff;
  box-shadow: 0 0 0.875912408759124vw rgba(16, 38, 73, 0.06);
  border-radius: 0.583941605839416vw;
  display: flex;
  align-items: center;
  padding: 0.656934306569343vw 1.16788321167883vw;
  grid-column: 1/5;
  grid-row: 1;
}
#menu_container #search_container #search_bar {
  padding: 0.145985401459854vw 7.01853284671533vw 0.145985401459854vw
    1.12296350364964vw;
  width: 28%;
  background: #f7f6f4;
  border-radius: 0.583941605839416vw;
  height: 4.08759124087591vw;
  position: relative;
  display: flex;
  align-items: center;
  height: 2.91970802919708vw;
}
#menu_container #search_container #search_bar input {
  width: 100%;
  height: 100%;
  font-weight: 500;
  font-size: 1.00729927007299vw;
  background: transparent;
  border: none;
  outline: none;
  padding: 0.510948905109489vw 0 0.510948905109489vw 0.875912408759124vw;
}
#menu_container #search_container #search_bar img {
  width: 1.34306569343066vw;
  height: 1.34306569343066vw;
  margin: auto;
}
#menu_container #button {
  display: flex;
  background: #0077d7;
  border-radius: 0.291970802919708vw;
  margin: auto 0 auto 19.7080291970803vw;
}
#menu_container #button button {
  background: transparent;
  outline: none;
  border: none;
  font-style: normal;
  font-weight: 500;
  font-size: 1.02189781021898vw;
  line-height: 1.60583941605839vw;
  color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}
#menu_container #button #btn1 {
  width: 10.2189781021898vw;
  height: 2.91970802919708vw;
  font-style: normal;
  font-weight: 500;
  font-size: 1.02189781021898vw;
  line-height: 1.60583941605839vw;
  color: #ffffff;
  justify-content: left;
}
#menu_container #button #btn1 img {
  margin: 0 0.72992700729927vw 0 0.875912408759124vw;
  width: 1.02189781021898vw;
  height: 1.02189781021898vw;
}
#menu_container #button #btn2 {
  width: 2.18978102189781vw;
  height: 2.91970802919708vw;
  border-left: 0.072992700729927vw solid white;
}
#menu_container #button #btn2 img {
  width: 1.02189781021898vw;
  height: 1.02189781021898vw;
}
#menu_container #profile {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto 0 auto auto;
}
#menu_container #profile #notification {
  width: 1.75182481751825vw;
  height: 1.75182481751825vw;
  margin: 0 1.60583941605839vw 0 0;
  cursor: pointer;
}
#menu_container #profile #avatar {
  width: 2.62773722627737vw;
  height: 2.62773722627737vw;
  border-radius: 50%;
  border: 0.145985401459854vw solid #0077d7;
  cursor: pointer;
}
#menu_container #profile p {
  margin: 0 0.364963503649635vw;
  font-style: normal;
  font-weight: normal;
  font-size: 0.875912408759124vw;
  color: #000000;
  cursor: pointer;
  display: flex;
  align-items: center;
}
#menu_container #profile p img {
  margin: 0 0 0 0.5vw;
  width: 1.02vw;
  height: 1.02vw;
}
#menu_container #inbox_container {
  width: 25.8394160583942vw;
  grid-column: 1/2;
  grid-row: 2;
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
  border: 0.0364963503649635vw solid #aaaaaa;
  box-sizing: border-box;
  border-radius: 0.291970802919708vw;
  width: 8.68613138686131vw;
  height: 2.62773722627737vw;
  font-style: normal;
  font-weight: bold;
  font-size: 1.02189781021898vw;
  line-height: 1.24087591240876vw;
  cursor: pointer;
}
#menu_container #inbox_container #ind_top button span {
  font-weight: 200;
}
#menu_container #inbox_container #ind_top button #drop {
  margin-left: 2.18978102189781vw;
  width:1.02vw;
  height:1.02vw;
}
#menu_container #inbox_container #ind_top button:nth-child(2) {
  width: 2.62773722627737vw;
  height: 2.62773722627737vw;
}
#menu_container #inbox_container #ind_top button:nth-child(2) img {
  width: 1.09489051094891vw;
  height: 1.09489051094891vw;
}
#menu_container #inbox_container #ind_middle {
  display: grid;
  grid-template-columns: 100%;
  gap: 1.31386861313869vw;
  margin: 1.31386861313869vw 0 0 0;
}
#menu_container #inbox_container #ind_middle #cards {
  background: #ffffff;
  box-shadow: 0 0 0.875912408759124vw rgba(16, 38, 73, 0.06);
  border-radius: 0.583941605839416vw;
  height: 10.2919708029197vw;
  padding: 1.16788321167883vw;
  transition: 0.5s ease-in-out;
}
#menu_container #inbox_container #ind_middle #cards:hover {
  border: 0.145985401459854vw solid #0077d7;
  box-shadow: 0 0 1.45985401459854vw rgba(18, 73, 164, 0.2);
}
#menu_container #inbox_container #ind_middle #cards #card_top {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
#menu_container #inbox_container #ind_middle #cards #card_top button {
  padding: 0.437956204379562vw 0.583941605839416vw;
  border: none;
  outline: none;
  font-style: normal;
  font-weight: 600;
  font-size: 0.72992700729927vw;
  cursor: pointer;
  border-radius: 0.291970802919708vw;
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
  font-size: 1.09489051094891vw;
}
#menu_container #inbox_container #ind_middle #cards #card_middle p {
  width: 23.5036496350365vw;
  font-style: normal;
  font-weight: 500;
  font-size: 1.02189781021898vw;
  line-height: 1.45985401459854vw;
  color: #200e32;
  margin-top: 0.72992700729927vw;
}
#menu_container
  #inbox_container
  #ind_middle
  #cards
  #card_middle
  p:nth-child(2) {
  font-style: normal;
  font-weight: normal;
  font-size: 0.875912408759124vw;
  line-height: 1.09489051094891vw;
  color: #200e32;
}
#menu_container
  #inbox_container
  #ind_middle
  #cards
  #card_middle
  p:nth-child(2)
  span {
  border: 0.072992700729927vw solid #200e32;
  padding: 0.109489051094891vw 0.437956204379562vw;
  border-radius: 0.218978102189781vw;
  margin: 0 0.364963503649635vw 0 0;
  font-weight: 600;
}
#menu_container #inbox_container #ind_middle #cards #card_bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 1vw 0 0 0;
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
  width: 2.18978102189781vw;
  height: 2.18978102189781vw;
  border-radius: 50%;
  border: 0.0510948905109489vw solid #0077d7;
  cursor: pointer;
}
#menu_container #inbox_container #ind_middle #cards #card_bottom #profile p {
  margin: 0 0.364963503649635vw;
  font-style: normal;
  font-weight: normal;
  font-size: 0.875912408759124vw;
  color: #000000;
  cursor: pointer;
}
#menu_container #inbox_container #ind_middle #cards #card_bottom button {
  padding: 0.141362773722628vw 0.565451824817518vw;
  border: none;
  outline: none;
  cursor: pointer;
  border-radius: 0.291970802919708vw;
  color: white;
  font-style: normal;
  font-weight: 500;
  font-size: 0.72992700729927vw;
  line-height: 1.09489051094891vw;
  display: flex;
  align-items: center;
  color: #ffffff;
  background: #16c45f;
}
#menu_container #inbox_container #ind_middle #cards #card_bottom button #clock {
  margin: 0 0.510948905109489vw 0 0;
  width: 0.72992700729927vw;
  height: 0.72992700729927vw;
}
#menu_container #inbox_container2 {
  grid-column: 2/5;
}

/*=============  Main Profile box=================*/
#inbox_container2 #inbox_container2_top {
  background: #ffffff;
  box-shadow: 0 0 0.875912408759124vw rgba(16, 38, 73, 0.06);
  border-radius: 0.583941605839416vw;
  display: flex;
  align-items: center;
  padding: 1.45985401459854vw 4.37956204379562vw 1.45985401459854vw
    1.45985401459854vw;
}
#inbox_container2 #inbox_container2_top #prof_img #avatar {
  width: 7.88321167883212vw;
  height: 7.88321167883212vw;
  border-radius: 50%;
  border: 0.218978102189781vw solid #41a4f3;
}
#inbox_container2 #inbox_container2_top #prof_data {
  margin: 0 0 0 0.72992700729927vw;
}
#inbox_container2 #inbox_container2_top #prof_data #id {
  font-style: normal;
  font-weight: normal;
  font-size: 0.875912408759124vw;
  line-height: 1.09489051094891vw;
  color: #200e32;
  display: flex;
  align-items: center;
}
#inbox_container2 #inbox_container2_top #prof_data #id span {
  border: 0.072992700729927vw solid #200e321a;
  padding: 0.109489051094891vw 0.437956204379562vw;
  border-radius: 0.218978102189781vw;
  margin: 0 0.364963503649635vw 0 0;
  font-weight: 600;
}
#inbox_container2 #inbox_container2_top #prof_data #id button {
  padding: 0.141362773722628vw 0.565451824817518vw;
  border: none;
  outline: none;
  cursor: pointer;
  border-radius: 0.291970802919708vw;
  color: white;
  font-style: normal;
  font-weight: 500;
  font-size: 0.72992700729927vw;
  line-height: 1.09489051094891vw;
  display: flex;
  align-items: center;
  color: #ffffff;
  background: #16c45f;
  margin: 0 0 0 2.18978102189781vw;
}
#inbox_container2 #inbox_container2_top #prof_data #id button #clock {
  margin: 0 0.510948905109489vw 0 0;
  width: 0.948905109489051vw;
  height: 0.948905109489051vw;
}
#inbox_container2 #inbox_container2_top #prof_data p:nth-child(2) {
  width: 32.8467153284672vw;
  font-style: normal;
  font-weight: 500;
  font-size: 1.16788321167883vw;
  line-height: 1.75182481751825vw;
  color: #200e32;
  margin: 0.875912408759124vw 0;
}
#inbox_container2 #inbox_container2_top #prof_data p:nth-child(3) {
  font-style: normal;
  font-weight: normal;
  font-size: 0.72992700729927vw;
  line-height: 0.875912408759124vw;
  color: #200e32;
}
#inbox_container2 #inbox_container2_top #prof_data #prof_btns {
  display: flex;
  justify-items: center;
  margin: 0.875912408759124vw 0 0 0;
}
#inbox_container2 #inbox_container2_top #prof_data #prof_btns p {
  display: flex;
  font-style: normal;
  font-weight: 500;
  font-size: 0.72992700729927vw;
  line-height: 1.75182481751825vw;
  color: #200e32;
  width: fit-content;
  margin: 0 0 0 4.01459854014599vw;
}
#inbox_container2 #inbox_container2_top #prof_data #prof_btns p span {
  padding: 0;
  width: fit-content;
  height: fit-content;
  margin: 0 0 0 0.583941605839416vw;
  border: none;
}
#inbox_container2 #inbox_container2_top #prof_data #prof_btns p:nth-child(1) {
  margin: 0;
}
#inbox_container2
  #inbox_container2_top
  #prof_data
  #prof_btns
  p:nth-child(1)
  span {
  font-style: normal;
  font-weight: 600;
  font-size: 0.72992700729927vw;
  line-height: 1.09489051094891vw;
  display: flex;
  align-items: center;
  color: #03a1b7;
  padding: 0.218978102189781vw 0.583941605839416vw;
  background: #e6fcff;
  border-radius: 0.291970802919708vw;
}
#inbox_container2
  #inbox_container2_top
  #prof_data
  #prof_btns
  p:nth-child(2)
  span {
  color: #0077d7;
}
#inbox_container2
  #inbox_container2_top
  #prof_data
  #prof_btns
  p:nth-child(3)
  span {
  color: #0077d7;
}

/*===============Tabs=========================*/
#inbox_container2 #inbox_container2_middle {
  display: flex;
  height: fit-content;
  background: #f2f8ff;
  justify-content: center;
}
#inbox_container2 #inbox_container2_middle p {
  font-style: normal;
  font-weight: 500;
  font-size: 1.01067153284672vw;
  line-height: 1.24087591240876vw;
  color: #200e32;
  opacity: 0.8;
  margin-left: 2.18978102189781vw;
  padding: 1.09489051094891vw 0;
  cursor: pointer;
  transition: 0.5s ease-in-out;
}
#inbox_container2 #inbox_container2_middle p:hover {
  border-bottom: 0.291970802919708vw solid #1e8bed;
  color: #1e8bed;
}
#inbox_container2 #inbox_container2_middle p:nth-child(1) {
  margin: 0;
}

/*====================Todo==========================*/
#inbox_container2 #inbox_container2_bottom {
  padding: 1.97080291970803vw 0;
  background: white;
}
#inbox_container2 #inbox_container2_bottom p {
  display: flex;
  align-items: center;
  font-style: normal;
  font-weight: bold;
  font-size: 1.01067153284672vw;
  line-height: 1.24087591240876vw;
  color: #65676d;
  padding: 0.948905109489051vw 1.09489051094891vw;
  border-bottom: 0.0510948905109489vw solid rgba(0, 0, 0, 0.1);
}
#inbox_container2 #inbox_container2_bottom p span {
  margin: 0 0 0 1.09489051094891vw;
  font-style: normal;
  font-weight: 500;
  font-size: 0.989540145985401vw;
}
#inbox_container2 #inbox_container2_bottom p:nth-child(1):nth-child(1) {
  font-style: normal;
  font-weight: bold;
  font-size: 1.12296350364964vw;
  line-height: 1.38686131386861vw;
  color: #000000;
  border: none;
}
#inbox_container2 #inbox_container2_bottom p:nth-child(1) span {
  color: #65676d;
  margin: 0 0 0 0.510948905109489vw;
}
#inbox_container2 #inbox_container2_bottom p #plus {
  width: 1.82481751824818vw;
  height: 1.82481751824818vw;
  margin: 0 0 0 auto;
  cursor: pointer;
}
</style>