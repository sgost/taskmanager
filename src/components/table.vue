<template>
  <div id="table_main">
    <div id="search_container">
      <div id="menu_b1">
        <img src="../assets/hamburger.svg" id="img2" />
        <img src="../assets/hotKup.svg" id="img1" />
      </div>
      <div id="search_bar">
        <img src="../assets/search.svg" />
        <input type="search" placeholder="search" />
      </div>
      <div id="profile">
        <img src="../assets/notification.svg" id="notification" />
        <img src="../assets/avatar.svg" id="avatar" />
        <p>Pavan B <img src="../assets/drop_black.svg" /></p>
      </div>
    </div>
    <div id="table_main_container">
      <div id="menu">
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
          <p>
            <img src="../assets/settings.svg" id="img1" />
            <img src="../assets/settings2.svg" id="img2" />SETTINGS
          </p>
        </div>
        <div id="menu_b3">
          <div id="button">
            <button id="btn1">
              <img src="../assets/pencil.svg" />New Task
            </button>
            <button id="btn2"><img src="../assets/drop_white.svg" /></button>
          </div>
          <div id="menu_b3_middle">
            <p>
              <span
                ><img src="../assets/message1.svg" id="img1" /><img
                  src="../assets/message2.svg"
                  id="img2"
                />Inbox</span
              ><span>(12)</span>
            </p>
            <p>
              <span
                ><img src="../assets/Send1.svg" id="img1" /><img
                  src="../assets/Send2.svg"
                  id="img2"
                />Sent</span
              ><span>(12)</span>
            </p>
            <p>
              <span
                ><img src="../assets/Close_Square.svg" id="img1" /><img
                  src="../assets/Close_Square2.svg"
                  id="img2"
                />Closed</span
              ><span>(12)</span>
            </p>
            <p>
              <span
                ><img src="../assets/Info.svg" id="img1" /><img
                  src="../assets/Info2.svg"
                  id="img2"
                />Overdue</span
              ><span>(12)</span>
            </p>
          </div>
          <div id="menu_b3_down">
            <h1>My Categories</h1>
            <p>Design<span>(6)</span></p>
            <p>Technology<span>(8)</span></p>
            <p>Finance<span>(2)</span></p>
          </div>
        </div>
      </div>

      <div id="menu_container">
        <div id="inbox_container">
          <div id="ind_top">
            <button>
              Inbox<span>(18)</span
              ><img src="../assets/drop_black.svg" id="drop" />
            </button>
            <button><img src="../assets/Filter.svg" /></button>
          </div>
          <div id="ind_middle">
            <div
            id="cards"
              v-bind:class="indToggle === index ? 'cards_active' : 'cards'"
              v-for="(inbox, index) in inbox"
              :key="index"
              @click="this.indToggle = index"
            >
              <div id="card_top">
                <button
                  v-bind:style="{
                    'background-color':
                      inbox.category === 'MAINTENANCE'
                        ? '#E6FCFF'
                        : inbox.category === 'DESIGN'
                        ? '#E6ECFF'
                        : inbox.category === 'RESEARCH'
                        ? '#F0F7E7'
                        : inbox.category === 'TRAVEL'
                        ? '#F9EBFD'
                        : '#E6FCFF',
                    color:
                      inbox.category === 'MAINTENANCE'
                        ? '#03A1B7'
                        : inbox.category === 'DESIGN'
                        ? '#367CEF'
                        : inbox.category === 'RESEARCH'
                        ? '#27AE60'
                        : inbox.category === 'TRAVEL'
                        ? '#EF2FAD'
                        : '#EF2FAD',
                  }"
                >
                  {{ inbox.category }}
                </button>
                <button>...</button>
              </div>
              <div id="card_middle">
                <p>{{ inbox.title }}</p>
                <p><span>#</span>Task ID: {{ index + 1 }}</p>
              </div>
              <div id="card_bottom">
                <div id="profile">
                  <img src="../assets/avatar.svg" id="avatar" />
                  <p>{{ inbox.name }}</p>
                </div>
                <button v-bind:style="{ 'background-color': inbox.date_color }">
                  <img src="../assets/clock.svg" id="clock" />07 AUG
                </button>
              </div>
            </div>
          </div>
        </div>

        <div
          id="inbox_container2"
          v-for="(inbox, index) in inbox"
          :key="index"
          v-bind:style="{ display: indToggle === index ? 'block' : 'none' }"
        >
          <div id="inbox_container2_top">
            <div id="prof_img">
              <img src="../assets/avatar.svg" id="avatar" />
            </div>
            <div id="prof_data">
              <p id="id">
                <span>#</span>Task ID: {{ index + 1 }}
                <button>
                  <img src="../assets/clock.svg" id="clock" />07 AUG
                </button>
              </p>
              <p>
                {{ inbox.title }}
              </p>
              <p>By Pawan Bhojanala, 12/11/2021, 5:42PM</p>
              <div id="prof_btns">
                <p>
                  CATEGORY:
                  <span
                    v-bind:style="{
                      'background-color':
                        inbox.category === 'MAINTENANCE'
                          ? '#E6FCFF'
                          : inbox.category === 'DESIGN'
                          ? '#E6ECFF'
                          : inbox.category === 'RESEARCH'
                          ? '#F0F7E7'
                          : inbox.category === 'TRAVEL'
                          ? '#F9EBFD'
                          : '#E6FCFF',
                      color:
                        inbox.category === 'MAINTENANCE'
                          ? '#03A1B7'
                          : inbox.category === 'DESIGN'
                          ? '#367CEF'
                          : inbox.category === 'RESEARCH'
                          ? '#27AE60'
                          : inbox.category === 'TRAVEL'
                          ? '#EF2FAD'
                          : '#EF2FAD',
                    }"
                    >{{ inbox.category }}</span
                  >
                </p>
                <p>STAGE: <span>NEW</span></p>
                <p>
                  ASSIGNEE: <span>{{ inbox.name }}</span>
                </p>
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
            <p @click="this.indToggle = 1">Hooks</p>
          </div>
          <div id="inbox_container2_bottom">
            <div id="task_bar_container" v-if="showTask">
              <input
                type="text"
                placeholder="Add Tasks"
                id="task_bar"
                v-model="message"
                @keyup.enter="add"
              />
              <img
                src="../assets/plus.svg"
                id="plus"
                @click="this.showTask = false"
              />
            </div>
            <p v-else>
              Checklist<span>({{ lists.length }})</span>
              <img
                src="../assets/plus.svg"
                id="plus"
                @click="this.showTask = true"
              />
            </p>

            <div id="lists">
              <p v-for="(Do, index) in lists" :key="index">
                {{
                  index === 0
                    ? "0" + (index + 1)
                    : index === 1
                    ? "0" + (index + 1)
                    : index === 2
                    ? "0" + (index + 1)
                    : index === 3
                    ? "0" + (index + 1)
                    : index === 4
                    ? "0" + (index + 1)
                    : index === 5
                    ? "0" + (index + 1)
                    : index === 6
                    ? "0" + (index + 1)
                    : index === 7
                    ? "0" + (index + 1)
                    : index === 8
                    ? "0" + (index + 1)
                    : index + 1
                }}<span>{{ Do }}</span
                ><img
                  src="../assets/checked.svg"
                  id="plus"
                  @click="remove(index)"
                />
                <img
                  src="../assets/checked_green.svg"
                  id="plus2"
                  @click="remove(index)"
                />
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Table",
  data() {
    return {
      message: "",
      inbox_toggle: 0,
      editing: false,
      editingId: 0,
      lists: ["Create Mobile Responsive Prototype for Task bench application"],
      inbox: [
        {
          category: "MAINTENANCE",
          title:
            "Please fix my computer network connection. Both LAN and Wi-Fi are not working",
          name: "Jack Smith",
          date_color: "#EB5757",
        },
        {
          category: "DESIGN",
          title:
            "Create Mobile Responsive Prototype for Task bench application",
          name: "Shirley Lynn",
          date_color: "#3DD193",
        },
        {
          category: "TRAVEL",
          title:
            "Please book a flight ticket to Johannesburg for 25th Aug 2021",
          name: "Pawan Bhojanala",
          date_color: "#FCAB3E",
        },
      ],
      showTask: false,
      indToggle: 0,
    };
  },
  methods: {
    add: function () {
      if (this.message !== "") {
        if (this.editing) {
          (this.lists[this.editingId] = this.message),
            (this.message = ""),
            (this.editing = false);
        } else {
          this.lists.push(this.message), (this.message = "");
        }
      }
    },

    remove: function (index) {
      this.lists.splice(index, 1);
    },

    edit: function (index) {
      this.message = this.lists[index];
      (this.editing = true), (this.editingId = index), (this.check = true);
    },
  },
};
</script>

<style scoped>
#table_main {
  padding: 0;
  height: 100vh;
  overflow: hidden;
}
@media (max-width: 1100px) {
  #table_main {
    padding: 0;
    height: 50vw;
  }
}
#table_main #search_container {
  background: #ffffff;
  box-shadow: 0 0 0.869565217391304vw rgba(16, 38, 73, 0.06);
  display: flex;
  align-items: center;
  padding: 0.656934306569343vw 1.16788321167883vw;
  margin: 0 0 0.072463768115942vw 0;
}
#table_main #search_container #menu_b1 {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.72992700729927vw 0.72992700729927vw 0.72992700729927vw 0.5vw;
}
#table_main #search_container #menu_b1 #img1 {
  width: 7.88321167883212vw;
  height: 1.8978102189781vw;
}
#table_main #search_container #menu_b1 #img2 {
  width: 2.33576642335766vw;
  height: 2.33576642335766vw;
  margin-right: 3.5036496350365vw;
  cursor: pointer;
}
#table_main #search_container #search_bar {
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
#table_main #search_container #search_bar input {
  width: 100%;
  height: 100%;
  font-weight: 500;
  font-size: 1.00729927007299vw;
  background: transparent;
  border: none;
  outline: none;
  padding: 0.510948905109489vw 0 0.510948905109489vw 0.875912408759124vw;
}
#table_main #search_container #search_bar img {
  width: 1.34306569343066vw;
  height: 1.34306569343066vw;
  margin: auto;
}
#table_main #profile {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto 0 auto auto;
}
#table_main #profile #notification {
  width: 1.75182481751825vw;
  height: 1.75182481751825vw;
  margin: 0 1.60583941605839vw 0 0;
  cursor: pointer;
}
#table_main #profile #avatar {
  width: 2.62773722627737vw;
  height: 2.62773722627737vw;
  border-radius: 50%;
  border: 0.145985401459854vw solid #0077d7;
  cursor: pointer;
}
#table_main #profile p {
  margin: 0 0.364963503649635vw;
  font-style: normal;
  font-weight: normal;
  font-size: 0.875912408759124vw;
  color: #000000;
  cursor: pointer;
  display: flex;
  align-items: center;
}
#table_main #profile p img {
  margin: 0 0 0 0.5vw;
  width: 0.8vw;
  height: 0.8vw;
}
#table_main_container {
  display: flex;
}
#menu {
  width: fit-content;
  height: 89vh;
  background: #ffffff;
  padding: 0;
  display: flex;
  overflow: hidden;
}
@media (max-width: 1100px) {
  #menu {
    height: 48vw;
  }
}
#menu #menu_b2 {
  width: 5.50724637681159vw;
  height: 100%;
  margin: 0;
  box-shadow: 0 0 0.869565217391304vw rgba(16, 38, 73, 0.1);
  padding: 3vw 0 0 0;
}
#menu #menu_b2 p {
  font-style: normal;
  font-weight: 600;
  font-size: 0.652173913043478vw;
  line-height: 1.09489051094891vw;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  color: #65676d;
  cursor: pointer;
  transition: 0.5s ease-in-out;
  padding: 0.579710144927536vw;
  position: relative;
  margin: 0.8vw 0 0 0;
}
#menu #menu_b2 p:nth-child(1) {
  margin: 0;
}
#menu #menu_b2 p:nth-child(7) {
  margin: 4vw 0 0 0;
}
#menu #menu_b2 p:hover:before {
  position: absolute;
  content: "";
  width: 0.144927536231884vw;
  height: 100%;
  right: 0;
  background: #0077d7;
}
#menu #menu_b2 p img {
  width: 1.44927536231884vw;
  height: 1.44927536231884vw;
  margin: 0;
  margin: 0 0 0.5vw 0;
}
#menu #menu_b2 p #img2 {
  display: none;
}
#menu #menu_b2 p:hover {
  background: #e6f2ff;
  color: #0077d7;
}
#menu #menu_b2 p:hover #img1 {
  display: none;
}
#menu #menu_b2 p:hover #img2 {
  display: block;
}

/*=================Side menu =======================*/
#menu #menu_b3 {
  width: 14.2028985507246vw;
  padding: 1.15942028985507vw;
}
#menu #menu_b3 #button {
  display: flex;
  width: fit-content;
  margin: auto;
}
#menu #menu_b3 #button button {
  background: #0077d7;
  border: none;
  outline: none;
  display: flex;
  height: 2.89855072463768vw;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  cursor: pointer;
  font-size: 1vw;
}
#menu #menu_b3 #button #btn1 {
  width: 8.91304347826087vw;
  border-radius: 0.579710144927536vw 0 0 0.579710144927536vw;
  justify-content: left;
}
#menu #menu_b3 #button #btn1 img {
  width: 1.44927536231884vw;
  height: 1.44927536231884vw;
  margin: 0 0.289855072463768vw 0 0.869565217391304vw;
}
#menu #menu_b3 #button #btn2 {
  width: 2.89855072463768vw;
  border-left: 0.072463768115942vw solid white;
  border-radius: 0 0.579710144927536vw 0.579710144927536vw 0;
}
#menu #menu_b3 #button #btn2 img {
  width: 0.579710144927536vw;
  height: 0.36231884057971vw;
}
#menu #menu_b3 #menu_b3_middle {
  margin: 2.89855072463768vw 0 0 0;
}
#menu #menu_b3 #menu_b3_middle p {
  margin: 0 0.364963503649635vw;
  font-style: normal;
  font-weight: normal;
  font-size: 0.869565217391304vw;
  color: #000000;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 1.30434782608696vw 0 0 0;
  padding: 0 0.579710144927536vw;
}
#menu #menu_b3 #menu_b3_middle p:hover {
  font-weight: bold;
  color: #0077d7;
}
#menu #menu_b3 #menu_b3_middle p span {
  display: flex;
  align-items: center;
}
#menu #menu_b3 #menu_b3_middle p img {
  width: 1.44927536231884vw;
  height: 1.44927536231884vw;
  margin: 0 0.5vw 0 0;
}
#menu #menu_b3 #menu_b3_middle p #img2 {
  display: none;
}
#menu #menu_b3 #menu_b3_middle p span:nth-child(2) {
  color: #200e32;
  opacity: 0.5;
}
#menu #menu_b3 #menu_b3_middle p:hover span:nth-child(2) {
  color: #0077d7;
}
#menu #menu_b3 #menu_b3_middle p:hover #img1 {
  display: none;
}
#menu #menu_b3 #menu_b3_middle p:hover #img2 {
  display: flex;
}

#menu #menu_b3 #menu_b3_down {
  margin: 2.89855072463768vw 0 0 0;
  padding: 0 0.579710144927536vw;
}

#menu #menu_b3 #menu_b3_down h1 {
  font-style: normal;
  font-weight: bold;
  font-size: 0.869565217391304vw;
  line-height: 1.08695652173913vw;
  color: #000000;
  padding: 0 0 0.869565217391304vw 0;
  border-bottom: 0.036231884057971vw solid #aaaaaa;
}
#menu #menu_b3 #menu_b3_down p {
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 0.869565217391304vw;
  line-height: 1.08695652173913vw;
  color: #200e32;
  opacity: 0.8;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0.869565217391304vw 0 0 0;
  cursor: pointer;
}
#menu #menu_b3 #menu_b3_down p:hover {
  color: #0077d7;
}

#menu #menu_b3 #menu_b3_down p span {
  opacity: 0.5;
}

/*=====================================================*/
#menu_container {
  width: 85%;
  height: 100%;
  margin: 1.15942028985507vw 1.15942028985507vw 0 1.15942028985507vw;
  display: grid;
  gap: 0.5vw;
  grid-template-columns: auto auto auto auto;
}
#menu_container #inbox_container {
  width: 25.8394160583942vw;
  grid-column: 1/2;
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
  width: 0.8vw;
  height: 0.8vw;
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
  height: 78vh;
  overflow: scroll;
}
@media (max-width: 1100px) {
  #menu_container #inbox_container #ind_middle {
    height: 39vw;
  }
}
#menu_container #inbox_container #ind_middle::-webkit-scrollbar {
  width: 3px;
}

#menu_container #inbox_container #ind_middle::-webkit-scrollbar-track {
  background: transparent;
}

#menu_container #inbox_container #ind_middle::-webkit-scrollbar-thumb {
  background: transparent;
}

#menu_container #inbox_container #ind_middle:hover::-webkit-scrollbar-thumb {
  background: rgba(85, 85, 85, 0.11);
}
#menu_container #inbox_container #ind_middle #cards {
  background: #ffffff;
  box-shadow: 0 0 0.875912408759124vw rgba(16, 38, 73, 0.06);
  border-radius: 0.583941605839416vw;
  height: 10.2919708029197vw;
  padding: 1.16788321167883vw;
  transition: 0.5s ease-in-out;
  cursor: pointer;
}
#menu_container #inbox_container #ind_middle .cards_active {
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
}
#menu_container #inbox_container #ind_middle #cards #card_bottom button #clock {
  margin: 0 0.510948905109489vw 0 0;
  width: 0.948905109489051vw;
  height: 0.948905109489051vw;
}

/*=============  Main Profile box=================*/
#menu_container #inbox_container2 {
  grid-column: 2/5;
}
#inbox_container2 #inbox_container2_top {
  background: #ffffff;
  box-shadow: 0 0 0.875912408759124vw rgba(16, 38, 73, 0.06);
  border-radius: 0.583941605839416vw;
  display: flex;
  align-items: center;
  padding: 1.45985401459854vw 4.37956204379562vw 0.8vw 1.45985401459854vw;
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
  margin: 0 0 0 2.2vw;
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
  font-size: 0.942028985507246vw;
  line-height: 1.24087591240876vw;
  color: #200e32;
  opacity: 0.8;
  margin-left: 1.9vw;
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
  padding: 1.97080291970803vw 1vw;
  background: white;
  position: relative;
}
#inbox_container2 #inbox_container2_bottom #task_bar_container {
  display: flex;
  justify-content: space-between;
  padding: 0 1vw;
}
#inbox_container2 #inbox_container2_bottom #task_bar_container #task_bar {
  width: 34.7101449275362vw;
  height: 3.33333333333333vw;
  background: #f3f3f3;
  border-radius: 0.579710144927536vw;
  border: none;
  outline: none;
  padding: 0 1vw;
  font-size: 1vw;
}
#inbox_container2 #inbox_container2_bottom #task_bar_container #plus {
  width: 1.82481751824818vw;
  height: 1.82481751824818vw;
  margin: auto 0 auto auto;
  cursor: pointer;
  transition: 0.5s ease-in-out;
  transform: rotate(45deg);
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
#inbox_container2 #inbox_container2_bottom p {
  font-style: normal;
  font-weight: bold;
  font-size: 1.12296350364964vw;
  line-height: 1.38686131386861vw;
  color: #000000;
  border: none;
}
#inbox_container2 #inbox_container2_bottom p span {
  color: #65676d;
  margin: 0 0 0 0.510948905109489vw;
}
#inbox_container2 #inbox_container2_bottom p #plus {
  width: 1.82481751824818vw;
  height: 1.82481751824818vw;
  margin: 0 0 0 auto;
  cursor: pointer;
  transition: 0.5s ease-in-out;
}
#inbox_container2 #inbox_container2_bottom #lists {
  overflow: scroll;
  height: 39vh;
}
#inbox_container2 #inbox_container2_bottom #lists::-webkit-scrollbar {
  width: 2px;
}

#inbox_container2 #inbox_container2_bottom #lists::-webkit-scrollbar-track {
  background: transparent;
}

#inbox_container2 #inbox_container2_bottom #lists::-webkit-scrollbar-thumb {
  background: transparent;
}

#inbox_container2
  #inbox_container2_bottom
  #lists:hover::-webkit-scrollbar-thumb {
  background: rgba(85, 85, 85, 0.11);
}
#inbox_container2 #inbox_container2_bottom #lists p {
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
#inbox_container2 #inbox_container2_bottom #lists p span {
  margin: 0 0 0 1.09489051094891vw;
  font-style: normal;
  font-weight: 500;
  font-size: 0.989540145985401vw;
  position: relative;
  color: black;
}
#inbox_container2 #inbox_container2_bottom #lists p #plus2 {
  width: 1.82481751824818vw;
  height: 1.82481751824818vw;
  margin: 0 0 0 auto;
  cursor: pointer;
  display: none;
}
#inbox_container2 #inbox_container2_bottom #lists p:hover span {
  color: #65676d;
}
#inbox_container2 #inbox_container2_bottom #lists p:hover #plus {
  display: none;
}
#inbox_container2 #inbox_container2_bottom #lists p:hover #plus2 {
  display: flex;
}
#inbox_container2 #inbox_container2_bottom #lists p:hover span:after {
  position: absolute;
  content: "";
  width: 100%;
  height: 0.072463768115942vw;
  background: #65676d;
  top: 49%;
  left: 0;
}
</style>