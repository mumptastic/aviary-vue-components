<template>
<a class="skip-to-content" href="#content">Skip to content</a>
<header aria-label="header">
  <div class="top-bar">
    <div class="container">
      <div class="logo">
        <a :href="`${logoHref}`">
            <span>
                <img :src="`${logo}`" :alt="`${title}`"/>
                <span class="mastTitle">{{mastTitle}}</span>
            </span>
        </a>
      </div>
      <div class="top-nav">
        <slot name="browNav"></slot>
      </div>
    </div>
  </div>
  <div class="masthead">
    <div class="container">
      <a :href="`${titleHref}`">
        <h1>{{title}}</h1>
      </a>
    </div>
  </div>
  <div class="bottom-nav">
    <div class="container">
      <slot name="mainNav"></slot>
    </div>
  </div>
</header>


</template>

<script>
export default {
  name: 'AviaryHeader',
  props: {
    logo: String,
    logoHref: {
        type: String,
        default: '#'
    },
    mastTitle:{
        type: String,
        default: "Texas A&M University Libraries"
    },
    titleHref: {
        type: String,
        default: 'https://library.tamu.edu'
    },
    title: {
        type: String,
        default: 'Aviary'
    },
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
          .skip-to-content {
            height: calc(var(--top-bar-height) - 10px);
            background: var(--top-bar-background);
            color: var(--top-bar-color);
            left: 5px;
            display: flex;
            position: absolute;
            align-items: center;
            padding: 0 12px;
            transform: translateY(-100%);
            transition: transform 0.3s;
            z-index: 2;
          }
  
          .skip-to-content:focus {
            margin-top: 4px;
            transform: translateY(2%);
          }
  
          .container {
            display: flex;
            height: 100%;
            padding: 0 calc(1.5rem * 0.5);
            margin: 0 auto;
          }
  
          @media (min-width: 576px) {
            .container {
              max-width: 540px;
            }
          }
          @media (min-width: 768px) {
            .container {
              max-width: 720px;
            }
          }
          @media (min-width: 992px) {
            .container {
              max-width: 960px;
            }
          }
          @media (min-width: 1200px) {
            .container {
              max-width: 1140px;
            }
          }
          @media (min-width: 1400px) {
            .container {
              max-width: 1320px;
            }
          }
  
          .top-bar {
            height: var(--top-bar-height);
            background: var(--top-bar-background);
            color: var(--top-bar-color);
            border-bottom: 1px solid var(--top-bar-border-color);
  
            .logo,
            .top-nav {
              display: flex;
              width: 100%;
              align-items: center;
            }
  
            .logo a {
              display: flex;
              color: var(--top-bar-color);
              text-decoration: none;
                img {
                  height: 36px;
                  width: 52px;
                  min-height: 36px;
                  min-width: 52px;
                }
              span {
                margin: auto 5px;
              }
              .mastTitle {
                position: relative;
                top: -10px;
              }

            }
  
            .top-nav {
              justify-content: right;
  
              
                nav > ul {
                  list-style: none;
                  margin: 0;
                  padding: 0;
                }
  
                nav > ul > li {
                  float: left;
                }
  
                nav > ul > li > a {
                  height: var(--top-bar-height);
                  color: var(--top-bar-color);
                  display: flex;
                  align-items: center;
                  padding: 0px 15px;
                  font-size: 14px;
                  text-decoration: none;
                }
  
                nav > ul > li:hover > a,
                nav > ul > li:focus-within > a {
                  background-color: var(--top-bar-hover-background);
                  color: var(--top-bar-hover-color);
                }
  
                nav > ul > li:not(:first-child) {
                  border-left: 1px solid var(--top-bar-border-color);
                }
  
                nav > ul > li.menu > ul[role=menu] {
                  opacity: 0;
                  visibility: hidden;
                  transition: opacity 0.25s, visibility 0s ease-in-out;
                  list-style: none;
                  position: absolute;
                  border: 1px solid var(--top-bar-border-color);
                  border-radius: 4px;
                  background-color: white;
                  color: black;
                  padding: 10px 15px;
                }
  
                nav > ul > li.menu > ul[role=menu] > li[role=presentation] {
                  padding: 10px;
                  a + div {
                    margin-top: 5px;
                    a {
                      color: #006483;
                    }
                    a:hover {
                      color: #004362;
                    }
                    span {
                      color: #707070;
                    }
                  }
                }
  
                nav > ul > li.menu > ul[role=menu] > li[role=presentation] > a[role=menuitem] {
                  text-decoration: none;
                  color: #3c0000;
                  display: flex;
                  align-items: center;
                  span {
                    margin-left: 6px;
                  }
                }
  
                nav > ul > li.menu:focus-within > ul[role=menu],
                nav > ul > li.menu:hover > ul[role=menu] {
                  opacity: 1;
                  visibility: visible;
                }
  
                @media (max-width: 1739.98px) {
                  nav > ul > li.menu > ul[role=menu].right-adjust {
                    right: 10px;
                  }
                }
  
              
            }
  
            @media (max-width: 991.98px) {
              .top-nav {
                display: none;
              }
            }
          }
  
          .masthead {
            height: var(--masthead-height);
            background: var(--masthead-background);
            color: var(--masthead-color);
            a {
              margin: auto 0;
              color: var(--masthead-color);
              text-decoration: none;
              h1 {
                font-size: var(--masthead-font-size);
                font-weight: var(--masthead-font-weigth);
                margin-block-start: 0;
                margin-block-end: 0;
                margin-inline-start: 0;
                margin-inline-end: 0;
              }
            }
          }
  
          
          .bottom-nav {
            background: var(--bottom-nav-background);
            color: var(--bottom-nav-color);
  
            
              nav > ul {
                list-style: none;
                margin: 0;
                padding: 0;
              }
  
              nav > ul > li {
                float: left;
              }
  
              nav > ul > li > a {
                height: var(--bottom-nav-height);
                color: var(--bottom-nav-color);
                display: flex;
                align-items: center;
                font-size: 16px;
                font-weight: 700;
                justify-content: center;
                text-decoration: none;
                width: 140px;
              }
  
              nav > ul > li:hover > a,
              nav > ul > li:focus-within > a {
                background-color: var(--bottom-nav-hover-background);
                color: var(--bottom-nav-hover-color);
              }
            
          }
  
          @media (max-width: 991.98px) {
            .bottom-nav {
              height: 40px;
            }
            .bottom-nav > .container {
              display: none;
            }
          }
        
  
  </style>