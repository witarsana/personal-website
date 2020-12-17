<template>
  <!-- Personal Website of Made Witarsana, koyoRoyo. Made by koyoRoyo in Bali, Indonesia -->
  <div
    id="app"
    class="flex overflow-auto xs:overflow-auto md:overflow-hidden xl:overflow-hidden text-gray-600 flex-col font- w-screen h-screen justify-between"
  >
    <!-- Header -->
    <div
      class="header xl:h-10 flex flex-col md:flex-row xl:flex-row items-center justify-between "
    >
      <div class="header-left text-2xl flex-1 font-hand px-4 py-1 h-10">
        Hi, could you help me to find the
        <span class="font-bold text-red-1000">menu</span> ? or
        <a
          target="_new"
          class="px-5 font-sans text-sm py-1 bg-yellow-500 rounded-full text-white "
          href="http://koyoroyo.com/game/"
          >play game instead</a
        >
      </div>
      <a
        class=" header-right w-full md:w-2/12 xl:w-2/12 justify-end md:justify-center xl:justify-center items-center flex bg-red-1000 text-white px-4 py-2 h-10 font-bold"
        href="#"
      >
        <span>
          <img class="w-6 logos" src="./assets/icon/logo.png" alt="" />
        </span>
        <span class="ml-2 font-sans">koyoRoyo</span>
      </a>
    </div>
    <!-- Header End Here -->
    <!-- Middle Section -->
    <div
      class="content bg-gray-1000 flex items-stretch  relative xs:relative md:static xl:static flex-1 px-3"
    >
      <!-- Grid Menu -->
      <transition name="showmenu">
        <div
          v-show="showMenu"
          id="grid-container"
          :class="
            showContent
              ? 'mx-auto absolute z-10 xs:absolute md:static xl:static xl:mx-0 xs:mx-auto md:mx-0'
              : 'static z-0 xs:static md:static xl:static mx-auto xs:mx-auto md:mx-auto xl:mx-auto'
          "
          class="content-container mt-5 "
        >
          <div
            id="menu4_container"
            :class="
              showContent
                ? 'hidden xs:hidden md:block xl:block'
                : 'block xs:block md:block xl:block'
            "
            class="g1 hover:opacity-75 cursor-pointer w-01  shadow-xl"
          >
            <div id="menu4_card">
              <div class="front face bg-gray-1001"></div>
              <div class="back face flex justify-center items-center ">
                <a
                  @click="show('Education')"
                  :class="
                    showContent
                      ? 'hidden xs:hidden md:block xl:block'
                      : 'block xs:block md:block xl:block'
                  "
                  class="text-base md:text-xl xl:text-2xl font-bold font-sans text-white"
                  href="#"
                  >Education</a
                >
              </div>
            </div>
          </div>
          <div
            class="g2  hover:opacity-75 cursor-pointer bg-gray-1001 shadow-xl"
          ></div>
          <div
            id="menu1_container"
            class="g3  cursor-pointer bg-gray-1000 shadow-xl"
          >
            <div id="menu1_card">
              <div class="front face bg-gray-1001"></div>
              <div class="back face flex justify-center items-center ">
                <a
                  @click="show('About')"
                  :class="
                    showContent
                      ? 'hidden xs:hidden md:block xl:block'
                      : 'block xs:block md:block xl:block'
                  "
                  class="text-base md:text-xl xl:text-2xl font-bold font-sans text-white"
                  href="#"
                  >About Me</a
                >
              </div>
            </div>
          </div>
          <div
            class="g4 relative hover:opacity-75 cursor-pointer bg-gray-1001 shadow-xl"
          >
            <div class="absolute w-full h-full">
              <img
                class="xl:hidden w-full h-full md:hidden"
                src="./assets/img/mobile/4.png"
              />
              <img
                class="sm:hidden xs:hidden w-full h-full md:block xl:block"
                src="./assets/img/web/4.png"
              />
            </div>
          </div>
          <div
            id="menu5_container"
            class="g5 relative hover:opacity-75 cursor-pointer shadow-xl"
          >
            <div id="menu5_card">
              <div class="front face bg-gray-1001">
                <img
                  class="xl:hidden w-full h-full md:hidden"
                  src="./assets/img/mobile/5.png"
                />
              </div>
              <div class="back face flex justify-center items-center ">
                <a
                  @click="show('Experience')"
                  :class="
                    showContent
                      ? 'hidden xs:hidden md:block xl:block'
                      : 'block xs:block md:block xl:block'
                  "
                  class="text-base md:text-xl xl:text-xl font-bold font-sans text-white"
                  href="#"
                  >Experience</a
                >
              </div>
            </div>
          </div>
          <div
            class="g6 hover:opacity-75 cursor-pointer bg-gray-1001 shadow-xl"
          ></div>
          <div
            id="menu2_container"
            class="g8  cursor-pointer bg-gray-1000 shadow-xl"
          >
            <div id="menu2_card">
              <div class="front face bg-gray-1001">
                <img
                  class="xl:hidden w-full h-full md:hidden"
                  src="./assets/img/mobile/3.png"
                />
                <img
                  class="sm:hidden xs:hidden w-full h-full md:block xl:block"
                  src="./assets/img/web/8.png"
                />
              </div>
              <div class="back face flex justify-center items-center ">
                <a
                  @click="show('Contact')"
                  :class="
                    showContent
                      ? 'hidden xs:hidden md:block xl:block'
                      : 'block xs:block md:block xl:block'
                  "
                  class="text-base md:text-xl xl:text-2xl font-bold font-sans text-white"
                  href="#"
                  >Contact</a
                >
              </div>
            </div>
          </div>
          <div
            class="g7 relative cursor-pointer hover:opacity-75 bg-gray-1001 shadow-xl"
          >
            <div class="absolute w-full h-full">
              <img
                class="sm:hidden xs:hidden w-full h-full md:block xl:block"
                src="./assets/img/web/7.png"
              />
            </div>
          </div>
          <div
            class="g9 relative cursor-pointer hover:opacity-75 bg-gray-1001 shadow-xl"
          >
            <div class="absolute w-full h-full">
              <img
                class="sm:hidden xs:hidden w-full h-full md:block xl:block"
                src="./assets/img/web/9.png"
              />
            </div>
          </div>
          <div
            id="menu3_container"
            class="g10  cursor-pointer bg-gray-1000 shadow-xl"
          >
            <div id="menu3_card">
              <div class="front face bg-gray-1001">
                <img
                  class="xl:hidden md:hidden w-full h-full"
                  src="./assets/img/mobile/6.png"
                />
              </div>
              <div class="back face flex justify-center items-center ">
                <a
                  @click="show('Latest Project')"
                  :class="
                    showContent
                      ? 'hidden xs:hidden md:block xl:block'
                      : 'block xs:block md:block xl:block'
                  "
                  class="text-base md:text-xl xl:text-2xl font-bold font-sans text-white"
                  href="#"
                  >Latest Project</a
                >
              </div>
            </div>
          </div>
        </div>
      </transition>
      <!-- Grid Menu End Here -->
      <!-- Content Start Here -->
      <transition name="showcontent">
        <div
          v-show="showContent"
          class="font-sans content-wrapper mt-5 px-5 py-5 flex justify-between flex-col flex-1 shadow-xl bg-white ml-0  xs:ml-0 md:ml-3 xl:ml-3"
        >
          <span
            class="block text-2xl text-gray-600 menu-name font-semibold border-b-2 border-gray-400"
            >{{ menuName }}</span
          >
          <!-- About Start Here -->
          <template v-if="menuName == 'About'">
            <div
              class="content project  mt-5 overflow-y-auto items-center xs:items-center  flex xs:flex md:block xl:block sm:flex-col xs:flex-col  flex-1"
            >
              <img
                class="rounded-full w-16 xs:w-16 md:w-24 xl:w-24 flex-none float-right"
                src="./assets/img/avatar.png"
                alt=""
              />
              <p class="mt-2 xs:mt-2 md:mt-0 xl:mt-0 ">
                Hi, My name is <b>Made Witarsana</b>. It's better You call me
                <b>"Koyo"</b>.<br /><br />
                Iam a <b>full stack developer</b> from
                <span class="text-red-1000">Bali</span>,
                <span class="text-red-1000">Indonesia</span>. <br /><br />
                I can Help You to make a <b>Website</b> or
                <b>Usefull Application</b> for Your business.<br /><br />
                Love playing drum, always dreaming if one day gonna be a
                <span class="text-red-1000">punk rock star</span> :)
              </p>
            </div>
          </template>
          <!-- About End Here -->
          <!-- Contact Start Here -->
          <template v-if="menuName == 'Contact'">
            <div class="content  mt-5 overflow-y-auto flex-1">
              <p>
                Send email to<br />
                <a
                  href="mailto:made.witarsana@gmail.com"
                  class="text-red-1000 hover:opacity-75"
                  ><b>made.witarsana@gmail.com</b></a
                >
                <br /><br />
                Or you cand find me on social media bellow
              </p>
              <ul class="flex items-center mt-3  text-red-1000">
                <li class="hover:opacity-75">
                  <a target="_new" href="https://web.facebook.com/koyo.rock">
                    <svg
                      class="fill-current"
                      x="0px"
                      y="0px"
                      width="38"
                      height="38"
                      viewBox="0 0 24 24"
                    >
                      <path
                        d="M12,2C6.477,2,2,6.477,2,12c0,5.013,3.693,9.153,8.505,9.876V14.65H8.031v-2.629h2.474v-1.749 c0-2.896,1.411-4.167,3.818-4.167c1.153,0,1.762,0.085,2.051,0.124v2.294h-1.642c-1.022,0-1.379,0.969-1.379,2.061v1.437h2.995 l-0.406,2.629h-2.588v7.247C18.235,21.236,22,17.062,22,12C22,6.477,17.523,2,12,2z"
                      ></path>
                    </svg>
                  </a>
                </li>
                <li class="ml-3 hover:opacity-75">
                  <a target="_new" href="https://www.instagram.com/witarsana/">
                    <svg
                      class="fill-current"
                      x="0px"
                      y="0px"
                      width="40"
                      height="40"
                      viewBox="0 0 24 24"
                    >
                      <path
                        d="M 8 3 C 5.243 3 3 5.243 3 8 L 3 16 C 3 18.757 5.243 21 8 21 L 16 21 C 18.757 21 21 18.757 21 16 L 21 8 C 21 5.243 18.757 3 16 3 L 8 3 z M 8 5 L 16 5 C 17.654 5 19 6.346 19 8 L 19 16 C 19 17.654 17.654 19 16 19 L 8 19 C 6.346 19 5 17.654 5 16 L 5 8 C 5 6.346 6.346 5 8 5 z M 17 6 A 1 1 0 0 0 16 7 A 1 1 0 0 0 17 8 A 1 1 0 0 0 18 7 A 1 1 0 0 0 17 6 z M 12 7 C 9.243 7 7 9.243 7 12 C 7 14.757 9.243 17 12 17 C 14.757 17 17 14.757 17 12 C 17 9.243 14.757 7 12 7 z M 12 9 C 13.654 9 15 10.346 15 12 C 15 13.654 13.654 15 12 15 C 10.346 15 9 13.654 9 12 C 9 10.346 10.346 9 12 9 z"
                      ></path>
                    </svg>
                  </a>
                </li>
                <li class="ml-3 hover:opacity-75">
                  <a
                    target="_new"
                    href="https://www.linkedin.com/in/made-witarsana-53906061/"
                  >
                    <svg
                      class="fill-current"
                      x="0px"
                      y="0px"
                      width="40"
                      height="40"
                      viewBox="0 0 24 24"
                    >
                      <path
                        d="M19,3H5C3.895,3,3,3.895,3,5v14c0,1.105,0.895,2,2,2h14c1.105,0,2-0.895,2-2V5C21,3.895,20.105,3,19,3z M9,17H6.477v-7H9 V17z M7.694,8.717c-0.771,0-1.286-0.514-1.286-1.2s0.514-1.2,1.371-1.2c0.771,0,1.286,0.514,1.286,1.2S8.551,8.717,7.694,8.717z M18,17h-2.442v-3.826c0-1.058-0.651-1.302-0.895-1.302s-1.058,0.163-1.058,1.302c0,0.163,0,3.826,0,3.826h-2.523v-7h2.523v0.977 C13.93,10.407,14.581,10,15.802,10C17.023,10,18,10.977,18,13.174V17z"
                      ></path>
                    </svg>
                  </a>
                </li>
                <li class="ml-3 hover:opacity-75">
                  <a target="_new" href="https://wa.me/6285792638226">
                    <svg
                      class="fill-current"
                      x="0px"
                      y="0px"
                      width="38"
                      height="38"
                      viewBox="0 0 24 24"
                    >
                      <path
                        d="M19.077,4.928C17.191,3.041,14.683,2.001,12.011,2c-5.506,0-9.987,4.479-9.989,9.985 c-0.001,1.76,0.459,3.478,1.333,4.992L2,22l5.233-1.237c1.459,0.796,3.101,1.215,4.773,1.216h0.004 c5.505,0,9.986-4.48,9.989-9.985C22.001,9.325,20.963,6.816,19.077,4.928z M16.898,15.554c-0.208,0.583-1.227,1.145-1.685,1.186 c-0.458,0.042-0.887,0.207-2.995-0.624c-2.537-1-4.139-3.601-4.263-3.767c-0.125-0.167-1.019-1.353-1.019-2.581 S7.581,7.936,7.81,7.687c0.229-0.25,0.499-0.312,0.666-0.312c0.166,0,0.333,0,0.478,0.006c0.178,0.007,0.375,0.016,0.562,0.431 c0.222,0.494,0.707,1.728,0.769,1.853s0.104,0.271,0.021,0.437s-0.125,0.27-0.249,0.416c-0.125,0.146-0.262,0.325-0.374,0.437 c-0.125,0.124-0.255,0.26-0.11,0.509c0.146,0.25,0.646,1.067,1.388,1.728c0.954,0.85,1.757,1.113,2.007,1.239 c0.25,0.125,0.395,0.104,0.541-0.063c0.146-0.166,0.624-0.728,0.79-0.978s0.333-0.208,0.562-0.125s1.456,0.687,1.705,0.812 c0.25,0.125,0.416,0.187,0.478,0.291C17.106,14.471,17.106,14.971,16.898,15.554z"
                      ></path>
                    </svg>
                  </a>
                </li>
              </ul>
            </div>
          </template>
          <!-- Contact End Here -->
          <!-- Lastest Project Start Here -->
          <template v-if="menuName == 'Latest Project'">
            <div
              class="content text-gray-700 flex-col flex h-64  overflow-hidden  mt-5  flex-1"
            >
              <div class="project overflow-y-auto tracking-wide ">
                <!--  -->
                <span
                  class="block font-bold text-red-1000 mb-3 flex items-center"
                >
                  <p class="mr-5">Movie Pick</p>
                  <a
                    class="bg-blue-400 hover:opacity-75 text-xs text-white px-2 py-2 rounded-lg"
                    href="http://koyoroyo.com/movie-pick"
                    target="_new"
                    >Live preview</a
                  >
                </span>
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/movie-pick.png"
                />
                <p class="mb-5">
                  Movie Pick is an application to discover your favorite movies,
                  get the information about a movie, rating, budget etc. You can
                  pick your favorite movie by click "Add favorite button". The
                  list of your favorite movies will saved in your local storage.
                  Yo can re-sort the list. Build using Angular and Tailwind CSS.
                  You can find the source on
                  <a
                    class=" text-blue-700"
                    href="https://github.com/witarsana/movie-pick"
                    target="_new"
                    >https://github.com/witarsana/movie-pick</a
                  >
                </p>
                <!-- -->
                <span
                  class="block font-bold text-red-1000 mb-3 flex items-center"
                >
                  <p class="mr-5">ZooBC Web Wallet</p>
                </span>
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/zoobc.png"
                />
                <p class="mb-5">
                  ZooBC Web Wallet is wallet for ZooBC. ZooBC is a blockchain
                  platform being implemented by Blockchain Zoo
                </p>
                <!--  -->
                <span
                  class="block font-bold text-red-1000 mb-3 flex items-center"
                >
                  <p class="mr-5">Inmotioon</p>
                  <a
                    class="bg-blue-400 hover:opacity-75 text-xs text-white px-2 py-2 rounded-lg"
                    href="http://inmotioon.com"
                    target="_new"
                    >Live preview</a
                  >
                </span>
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/inmotioons.png"
                />
                <p class="mb-5">
                  Inmotioon.com is a provider for online digital invitation.
                  Located in Bali Indonesia.
                </p>
                <!--  -->
                <span
                  class="block font-bold text-red-1000 mb-3 flex items-center"
                >
                  <p class="mr-5">Custom Admin</p>
                  <a
                    class="bg-blue-400 hover:opacity-75 text-xs text-white px-2 py-2 rounded-lg"
                    href="http://koyoroyo.com/custom-admin"
                    target="_new"
                    >Live preview</a
                  >
                </span>
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/custom-admin.png"
                />
                <p class="mb-5">
                  An admin template, I made it inspired by Gmail UI. I love
                  Gmail UI who look very simple and clean. I made it using Vue,
                  Sass, and Tailwind CSS
                </p>
                <!--  -->
                <span
                  class="block font-bold text-red-1000 mb-3 flex items-center"
                >
                  <p class="mr-5">Custom UI</p>
                  <a
                    class="bg-blue-400 hover:opacity-75 text-xs text-white px-2 py-2 rounded-lg"
                    href="http://koyoroyo.com/custom-ui"
                    target="_new"
                    >Live preview</a
                  >
                </span>
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/design-ui.png"
                />
                <p class="mb-5">
                  An admin template, Admin LTE Alternative inspired by WPS
                  Office UI. I made it using Vue.js and Tailwind CSS. Resource
                  will be available at GitHub and you can download it soon.
                </p>
                <!--  -->
                <span class="block font-bold text-red-1000 mb-3"
                  >HRIS Application</span
                >
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/hris.png"
                />
                <p class="mb-5">
                  HRIS Application is an Human Resource Information System.
                  Handle the employee, payroll, tax etc. Made with Vue JS and
                  Bootstrap on the Front End and laravel as a Backend.
                </p>
                <!--  -->
                <span class="block font-bold text-red-1000 mb-3">SIADES</span>
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/sia.png"
                />
                <p class="mb-5">
                  SIADES is an Administration Application for village government
                  to make their annual budget (APBDES).
                </p>
                <!--  -->
                <span class="block font-bold text-red-1000 mb-3"
                  >Sirenbangda Eksekutif</span
                >
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/sirenbangda.png"
                />
                <p class="mb-5">
                  Sirenbangda Eksekutif is a Dashboard that show the information
                  of budget from a district government in Bali
                </p>
                <!--  -->
                <span class="block font-bold text-red-1000 mb-3"
                  >blibarang.id</span
                >
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/blibarang.png"
                />
                <p class="mb-5">
                  blibarang.id is an e-commerce that sell daily needs, located
                  in Jakarta, Indonesia. I made it using Opencart CMS
                </p>
                <!--  -->
                <span
                  class="block font-bold text-red-1000 mb-3 flex items-center"
                >
                  <p class="mr-5">Queue Application</p>
                </span>
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/queue1.png"
                />
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/queue2.png"
                />
                <p class="mb-5">
                  This application handles the customer queues of a Bank in
                  Indonesia. I made it using VB .NET 2010. The application is
                  used for their Bank in Bali and Nusa Tenggara.
                </p>
                <!--  -->
                <span class="block font-bold text-red-1000 mb-3">e-Persal</span>
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/e-talent2.png"
                />
                <p class="mb-5">
                  e-Persal is an Information System owned by TNI AL (Indonesian
                  Navy). This application used for check their member
                  background, history of education, family etc.
                </p>
                <!--  -->
                <span class="block font-bold text-red-1000 mb-3"
                  >Mahpati Website</span
                >
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/mahpati.png"
                />
                <p class="mb-5">
                  I made a company website for PT. Mahpati Inti Solusindo. A
                  Software Company in Jakarta.
                </p>
                <!--  -->
                <span class="block font-bold text-red-1000 mb-3">E-Office</span>
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/eoffice.png"
                />
                <p class="mb-5">
                  This Application handle correspondence in KODIKLATAL,
                  Surabaya. The schooll owned by Indonesian Navy.
                </p>
                <!--  -->
                <span class="block font-bold text-red-1000 mb-3"
                  >Sisinfodik</span
                >
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/sisinfodik.png"
                />
                <p class="mb-5">
                  Sisinfodik or "Sistem Informasi Pendidikan" is an Information
                  System that handle two school owned by Indonesian Navy, that
                  is KODIKLATAL(Surabaya) and SESKOAL(Jakarta). This system
                  handle student, teacher, and curriculum.
                </p>
                <!--  -->
                <span class="block font-bold text-red-1000 mb-3">Pesud</span>
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/pesud.png"
                />
                <p class="mb-5">
                  Pesud is an Information System that handle the Airplane data
                  of Indonesian Navy.
                </p>
                <!--  -->
                <span class="block font-bold text-red-1000 mb-3"
                  >Mr Buttler</span
                >
                <img
                  class="mb-2 shadow-xl"
                  src="./assets/img/portofolio/buttler.png"
                />
                <p class="mb-5">
                  Mr. Buttler is an Hotel Information System that handles
                  bookings, rooms, restaurant and guest transactions during
                  their stay.
                </p>
              </div>

              <!--  -->
            </div>
          </template>
          <!-- Latest Project End Here -->
          <!-- Education Start Here -->
          <template v-if="menuName == 'Education'">
            <div
              class="content text-gray-700 flex-col flex h-64  overflow-hidden  mt-5  flex-1"
            >
              <ul class="text-gray-600 text-sm md:text-base xl:text-base">
                <li class="flex justify-between items-center mb-5">
                  <span class="h-10 w-2 bg-red-1000 rounded"></span>
                  <span class="flex flex-1 flex-col ml-8">
                    <p class="font-semibold">STMIK STIKOM Indonesia</p>
                    <p>2009 - 2013</p>
                  </span>
                  <span class="self-start text-sm text-red-1000">College</span>
                </li>
                <li class="flex justify-between items-center mb-5">
                  <span class="h-10 w-2 bg-red-1000 rounded"></span>
                  <span class="flex flex-1 flex-col ml-8">
                    <p class="font-semibold">SMAN 1 Abiansemal</p>
                    <p>2006 - 2009</p>
                  </span>
                  <span class="self-start text-sm text-red-1000"
                    >Senior High School</span
                  >
                </li>
                <li class="flex justify-between items-center mb-5">
                  <span class="h-10 w-2 bg-red-1000 rounded"></span>
                  <span class="flex flex-1 flex-col ml-8">
                    <p class="font-semibold">SMPN 1 Abiansemal</p>
                    <p>2003 - 2006</p>
                  </span>
                  <span class="self-start text-sm text-red-1000"
                    >Junior High School</span
                  >
                </li>
                <li class="flex justify-between items-center mb-5">
                  <span class="h-10 w-2 bg-red-1000 rounded"></span>
                  <span class="flex flex-1 flex-col ml-8">
                    <p class="font-semibold">SDN 8 Carangsari</p>
                    <p>1997 - 2003</p>
                  </span>
                  <span class="self-start text-sm text-red-1000"
                    >Elementary School</span
                  >
                </li>
              </ul>
            </div>
          </template>
          <!-- Education End Here -->
          <!-- Experience -->
          <template v-if="menuName == 'Experience'">
            <div
              class="content text-gray-700 flex-col flex h-64  overflow-hidden  mt-5  flex-1"
            >
              <ul class="overflow-y-auto project">
                <li class="py-2 px-2 border-b border-gray-300 ">
                  <span class="text-red-1000 text-sm font-semibold"
                    >March 2020 - Now</span
                  >
                  <span class="flex justify-between">
                    <p class="font-bold  text-gray-600">Blockchain Zoo</p>
                    <p class="text-red-1000 text-sm w-1/3">
                      Frontend Developer
                    </p>
                  </span>
                </li>
                <li class="py-2 px-2 border-b border-gray-300 ">
                  <span class="text-red-1000 text-sm font-semibold"
                    >Jan 2020 - Now</span
                  >
                  <span class="flex justify-between">
                    <p class="font-bold  text-gray-600">Freelance</p>
                    <p class="text-red-1000 text-sm w-1/3">
                      Full Stack Developer
                    </p>
                  </span>
                </li>
                <li class="py-2 px-2 border-b border-gray-300 ">
                  <span class="text-red-1000 text-sm font-semibold"
                    >Oct 2019 - Jan 2020</span
                  >
                  <span class="flex justify-between">
                    <p class="font-bold  text-gray-600">
                      PT Mahpati Solusindo (South Jakarta)
                    </p>
                    <p class="text-red-1000 text-sm w-1/3">Backend Engineer</p>
                  </span>
                </li>
                <li class="py-2 px-2 border-b border-gray-300 ">
                  <span class="text-red-1000 text-sm font-semibold"
                    >Jan 2017 - October 2019</span
                  >
                  <span class="flex justify-between">
                    <p class="font-bold  text-gray-600">
                      PT Mahpati Solusindo (South Jakarta)
                    </p>
                    <p class="text-red-1000 text-sm w-1/3">
                      Software Developer
                    </p>
                  </span>
                </li>
                <li class="py-2 px-2 border-b border-gray-300 ">
                  <span class="text-red-1000 text-sm font-semibold"
                    >Aug 2015 - Dec 2016</span
                  >
                  <span class="flex justify-between">
                    <p class="font-bold  text-gray-600">
                      PT Dimata Sora Jayate
                    </p>
                    <p class="text-red-1000 text-sm w-1/3">
                      Software Developer
                    </p>
                  </span>
                </li>
                <li class="py-2 px-2 border-b border-gray-300 ">
                  <span class="text-red-1000 text-sm font-semibold"
                    >Dec 2013 - Jul 2015</span
                  >
                  <span class="flex justify-between">
                    <p class="font-bold  text-gray-600">
                      PT Evo Solusi Indonesia
                    </p>
                    <p class="text-red-1000 text-sm w-1/3">
                      Software Developer
                    </p>
                  </span>
                </li>
                <li class="py-2 px-2 border-b border-gray-300 ">
                  <span class="text-red-1000 text-sm font-semibold"
                    >Sep 2013 - Dec 2013</span
                  >
                  <span class="flex justify-between">
                    <p class="font-bold  text-gray-600">Serela Kuta Hotel</p>
                    <p class="text-red-1000 text-sm w-1/3">Night Auditor</p>
                  </span>
                </li>
                <li class="py-2 px-2 border-b border-gray-300 ">
                  <span class="text-red-1000 text-sm font-semibold"
                    >Feb 2013 - Jun 2013</span
                  >
                  <span class="flex justify-between">
                    <p class="font-bold  text-gray-600">Light and Pulse</p>
                    <p class="text-red-1000 text-sm w-1/3">Web Programmer</p>
                  </span>
                </li>
                <li class="py-2 px-2 border-b border-gray-300 ">
                  <span class="text-red-1000 text-sm font-semibold"
                    >Mar 2011 - Aug 2011</span
                  >
                  <span class="flex justify-between">
                    <p class="font-bold  text-gray-600">iPhone Bali</p>
                    <p class="text-red-1000 text-sm w-1/3">Technician</p>
                  </span>
                </li>
              </ul>
            </div>
          </template>
          <!-- Experience -->
          <div class="text-right">
            <button
              @click="hideMenu"
              class="w-12 h-12 bg-red-1000 rounded-xl text-white"
            >
              <svg
                class="fill-current"
                width="48"
                height="48"
                viewBox="0 0 48 48"
              >
                <title>Hide</title>
                <path
                  d="M20 12l-2.83 2.83L26.34 24l-9.17 9.17L20 36l12-12z"
                ></path>
              </svg>
            </button>
          </div>
        </div>
      </transition>
      <!-- Content End Here -->
    </div>
    <!-- Middle Section End Here -->
    <!-- Footer Start Here -->
    <div class="footer bg-gray-1000 flex pt-5">
      <div
        class="foot font-sans w-full xl:w-1/5 md:w-2/5 text-center text-sm bg-red-1000 py-2 text-white mx-auto px-10 h-10"
      >
        Copyright &copy koyoRoyo 2020
      </div>
    </div>
    <!-- Footer End Here -->
  </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      showMenu: false,
      showContent: false,
      menuName: "",
    };
  },
  methods: {
    show(name) {
      this.showContent = true;
      this.menuName = name;
    },
    hideMenu() {
      this.showContent = false;
      this.menuName = "";
    },
  },
  mounted() {
    this.showMenu = true;
  },
};
</script>
<style scoped></style>
