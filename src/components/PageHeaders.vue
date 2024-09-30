 <template>
    <div class="header">
      <div class="left_content">
        <button @click="toggleDrawer">
            <PageIcons iconType="star" color="#886CC0"></PageIcons>
        </button>
        <h2>Messages</h2>
        <PageDrawer ref="drawer">
          <h2>Drawer Content</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </PageDrawer>
      </div>
  
      <div class="right_content">
        <SearchBar></SearchBar>
        <PageBadge :value="76" color="pink">
            <PageIcons iconType="star"></PageIcons>
        </PageBadge>
        <PageBadge :value="12" color="gold">
            <PageIcons iconType="bell"></PageIcons>
        </PageBadge>
        <PageBadge :value="76" color="red">
            <PageIcons iconType="message"></PageIcons>
        </PageBadge>
        <PageBadge :value="1" color="green">
            <PageIcons iconType="date"></PageIcons>
        </PageBadge>
        <UserPortFolio :profile-image="require('@/assets/user.jpg')" :width="110" :height="50" class="user"></UserPortFolio>
      </div>
    </div>
  </template>
  
  <script>
  import SearchBar from './SearchBar.vue';
  import UserPortFolio from './UserPortfolio.vue';
  import PageIcons from './PageIcons.vue';
  import PageDrawer from './PageDrawer.vue';
  import PageBadge from './PageBadge.vue';

  
  export default {
    components: {
    SearchBar,
    UserPortFolio,
    PageIcons,
    PageDrawer,
    PageBadge,
},
    props: {
      items: {
        type: Array,
        required: true,
      },
      logoText: {
        type: String,
        default: "Navbar",
      },
      isMobile: {
        type: Boolean,
        default: false,
      },
    },
    data() {
      return {
        menuVisible: false,
      };
    },
    methods: {
      toggleMenu() {
        this.menuVisible = !this.menuVisible;
        const hamburgerLines = document.querySelector(".hamburger-lines");
        hamburgerLines.classList.toggle("active", this.menuVisible);
      },
    },
  };
  </script>
  
  <style scoped>
  .header {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: var(--primary-bg);
    box-shadow: var(--box-shadow);
    padding: 15px;
    border-radius: var(--border-radius);
    padding:5px 50px;
    border-bottom: 1px solid #9f9f9f;
  }

  
  .left_content{
    display: flex;
    align-items: center;
    gap: 30px;
    background-color: var(--primary-bg);
  }
  
  button {
    padding: 10px;
    font-size: 16px;
    color: #886CC0;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .right_content{
    display: flex;
    align-items: center;
    gap: 35px;
  }
  

  </style>