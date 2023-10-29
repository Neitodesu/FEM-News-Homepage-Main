<script>
  const mainLogo = 'logo.svg';
  const mobileMenu = 'icon-menu.svg';
</script>

<header class="container">
  <div>
    <img src={mainLogo} alt="">
  </div>
  <div class="nav-links">
    <li><a href="/">Home</a></li>
    <li><a href="/">New</a></li>
    <li><a href="/">Popular</a></li>
    <li><a href="/">Trending</a></li>
    <li><a href="/">Categories</a></li>
  </div>
  <div class="mobile-menu">
    <img class="mobile-button" src={mobileMenu} alt="">
  </div>
</header>

<style lang="scss">
  .container{
    width: 100%;
    padding-block: 1em;
    display: flex;
    align-items: center;
    justify-content: space-between;

    img{
      min-width: 2px;
    }

    .nav-links{
      display: none;
      
      @media screen and (min-width: 800px) {
        display: flex;
        gap: 2.35em;
        align-items: center;
        justify-content: center;
      }
    }

    .mobile-menu{
      @media screen and (min-width: 800px) {
        display: none;
      }

      .mobile-button{
        border: 0;

        &:hover{
          cursor: pointer;
        }
      }
    }
  }

  a{
    color: var(--darkGrayishBlue);
    text-decoration: none;

    &:hover{
      color: var(--softRed);
    }
  }
</style>