<template>
 <Header logo="https://api.library.tamu.edu/tl-components/1.12/assets/icons/tl/tamu-logo.svg" title="Aviary Components">
  <template v-slot:browNav>
    <nav>
        <ul>
          <li><a href="//library.tamu.edu/about/hours">Hours</a></li>
          <li class="menu">
            <a href="//library.tamu.edu/about/index">Libraries</a>
            <ul role="menu">
              <li role="presentation">
                <a href="//blcc.library.tamu.edu" title="Go to Business Library and Collaboration Commons website">Business Library & Collaboration Commons</a>
                <a class="directions" href="//library.tamu.edu/about/directions/business-library" title="Parking Directions for Business Library and Collaboration Commons">Parking Directions</a>
                <span class="phone">979-845-2111</span>
              </li>
              <li role="presentation">
                <a href="//cushing.library.tamu.edu" title="Go to Cushing Library website">Cushing Memorial Library & Archives</a>
                <a class="directions" href="//library.tamu.edu/about/directions/cushing-library" title="Parking Directions for Cushing Library">Parking Directions</a>
                <span class="phone">979-845-1951</span>
              </li>
              <li role="presentation">
                <a href="//msl.library.tamu.edu" title="Go to Medical Sciences Library website">Medical Sciences Library</a>
                <a class="directions" href="//library.tamu.edu/about/directions/medical-sciences-library" title="Parking Directions for Medical Sciences Library">Parking Directions</a>
                <span class="phone">979-845-7428</span>
              </li>
              <li role="presentation">
                <a href="//psel.library.tamu.edu" title="Go to Policy Sciences and Economics Library website">Policy Sciences & Economics Library</a>
                <a class="directions" href="//library.tamu.edu/about/directions/policy-sciences-economics-library" title="Parking Directions for Policy Sciences and Economics Library">Parking Directions</a>
                <span class="phone">979-845-3731</span>
              </li>
              <li role="presentation">
                <a href="//library.tamu.edu" title="Go to Evans Library website">Sterling C. Evans Library & Annex</a>
                <a class="directions" href="//library.tamu.edu/about/directions/evans-library-annex" title="Parking Directions for Evans Library and Annex">Parking Directions</a>
                <span class="phone">979-845-3731</span>
              </li>
            </ul>
          </li>
          <li class="menu">
            <a href="//library.tamu.edu">Information for</a>
            <ul role="menu">
              <li role="presentation">
                <a role="menuitem" href="//library.tamu.edu/faculty_info">Information for Faculty</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="//library.tamu.edu/grad_info">Graduate Student Resources</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="//library.tamu.edu/undergrad_info">Undergraduate Student Resources</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="//library.tamu.edu/services/accessibility">Services for Individuals with Disabilities</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="//tamu.libguides.com/c.php?g=949823">Students at Satellite Campuses</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="//tamu.libguides.com/c.php?g=586101&amp;p=4048709">School Visitors</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="//library.tamu.edu/about/other_patrons">Other Library Guests (Non-TAMU Affiliates)</a>
              </li>
            </ul>
          </li>
          <li><a href="//library.tamu.edu/mylibrary">MyLibrary</a></li>
          <li class="menu">
            <a href="//askus.library.tamu.edu">Help</a>
            <ul role="menu">
              <li role="presentation">
                <a role="menuitem" href="//askus.library.tamu.edu">Chat with us</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="//library.tamu.edu/about/phone">Call us</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="sms:9792561091">Text us @ 979-256-1091</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="//askus.library.tamu.edu/contact">Email us</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="//askus.library.tamu.edu">FAQs</a>
              </li>
              <li role="presentation">
                <a role="menuitem" href="//askus.library.tamu.edu/contact">Report a problem</a>
              </li>
            </ul>
          </li>
        </ul>
    </nav>
  </template>

  <template v-slot:mainNav>
    <nav role="navigation" aria-label="Header bottom navigation">
      <ul>
        <li><a href="#test">Services</a></li>
        <li><a href="#test">Research</a></li>
        <li><a href="#test">Visit &amp; Study</a></li>
        <li><a href="#test">Collections</a></li>
      </ul>
    </nav>
  </template>
 </Header>

 <div class="content"></div>

 <Footer>
  <template v-slot:Footernav>
    <nav role="navigation" aria-label="Footer navigation">
      <ul>
        <li>
          <a href="//howdy.tamu.edu/uPortal/normal/render.uP">howdy.tamu.edu</a>
        </li>
        <li>
          <a href="//library.tamu.edu/services/tech_troubleshooting.html">Off-Campus Access</a>
        </li>
        <li>
          <a href="//tamu.edu">Texas A& M University</a>
        </li>
        <li>
          <a href="//library.tamu.edu/about/compliance.html">Site Policies</a>
        </li>
        <li>
          <a href="//library.tamu.edu/services/accessibility.html">Accessibility</a>
        </li>
        <li>
          <a href="//www.thecb.state.tx.us/apps/txcrews/">Texas CREWS</a>
        </li>
        <li>
          <a href="//askus.library.tamu.edu/contact/index">Comments</a>
        </li>
        <li>
          <a href="//library.tamu.edu/status">Services Status</a>
        </li>
      </ul>
    </nav>
  </template>
 </Footer>
</template>

<script>
import './assets/style.scss'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss">
  
.content {
  min-height: calc(100vh - 50px);
}
</style>