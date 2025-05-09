<template>
  <div class="app">
    
    <!-- Header -->
    <div class="prezent-container">
    <!-- Navigation Header -->
    <header class="nav-header">
      <div class="logo">
        <img src="https://cdn.prod.website-files.com/6299214533322116e7c4b016/650987af31111e74b1cc42e0_Group%201000001092.svg" alt="Prezent Logo" />
      </div>
      <nav class="main-nav">
        <div class="nav-items">
          <div class="nav-item">
            Platform
          </div>
          <div class="nav-item">
            Services
          </div>
          <div class="nav-item">
            Solutions
          </div>
          <div class="nav-item">
            Resources
          </div>
          <div class="nav-item">
            About
          </div>
          <div class="nav-item">Login</div>
        </div>
      </nav>
      <div class="cta-buttons">
        <button class="btn btn-outline">Schedule a demo</button>
        <button class="btn btn-primary">Try for free</button>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
      <section class="fingerprint-hero-section">
     <div class="_1280w w-container">
      <div class="fp-hero-container">
        <div id="discover-your-fingerprint" class="fp-hero-left-content">
          <h1 class="fp-hero-heading">What's your communication fingerprint?</h1>
          <p class="fp-hero-parag">
            Shape a unique way of communicating that's distinctly yours, making your prezentations stand out and ensure they click with your audience and team.
          </p>
          <form class="fing-form" @submit.prevent="submitForm">
            <input
              class="fing-field"
              placeholder="Work Email"
              type="email"
              v-model="email"
              required
            />
            <input
              class="fing-submit"
              type="submit"
              :value="isSubmitting ? 'Submitting...' : 'Discover your Fingerprint'"
              :disabled="isSubmitting"
            />
          </form>
        </div>

        <div class="fp-hero-right-ing">
          <img
            src="https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b52623cdc21789daf960f6_Group%20138.webp"
            loading="lazy"
            sizes="(max-width: 827px) 100vw, (max-width: 991px) 95vw, 529px"
            srcset="
              https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b52623cdc21789daf960f6_Group%20138-p-500.webp 500w,
              https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b52623cdc21789daf960f6_Group%20138-p-800.webp 800w,
              https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b52623cdc21789daf960f6_Group%20138-p-1080.webp 1080w,
              https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b52623cdc21789daf960f6_Group%20138.webp 1257w
            "
            alt="fingerprint hero banner"
            class="fp-hero-img"
          />
        </div>
      </div>
    </div>
    </section>
  </section>

    <section class="fingerprints-video-section">
      <div class="_1280w w-container">
        <div class="fp-video-container">
          <div style="padding-top:56.27659574468085%" class="video-4 w-video w-embed">
            <iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fplayer.vimeo.com%2Fvideo%2F861693137%3Fapp_id%3D122963&amp;dntp=1&amp;display_name=Vimeo&amp;url=https%3A%2F%2Fvimeo.com%2F861693137&amp;image=https%3A%2F%2Fi.vimeocdn.com%2Fvideo%2F1720294709-79508bf4ef5e1d2c659be9bbb5a990492f554fddf5f27540bdd9f5fa2e00fef8-d_1280&amp;key=c4e54deccf4d4ec997a64902e9a30300&amp;type=text%2Fhtml&amp;schema=vimeo" scrolling="no" allowfullscreen="" title="fingerprints">
            </iframe>
          </div>
        </div>
      </div>
    </section>

    <div class="communication-fingerprint">
    <h1 class="title">Why create a communication fingerprint</h1>
    
    <div class="benefits-container">
      <!-- First Benefit -->
      <div class="benefit-card">
        <div class="card-content">
          <div class="image-container">
            <img src="https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b52b48cdc21789daff9064_Group%20138.svg" alt="Person analyzing data with magnifying glass" />
          </div>
          <h2 class="benefit-title">Know yourself</h2>
          <p class="benefit-description">
            Become self-aware as a communicator. Use your strengths effectively. 
            Help others tailor their messages to your needs.
          </p>
        </div>
      </div>
      
      <!-- Second Benefit -->
      <div class="benefit-card">
        <div class="card-content">
          <div class="image-container">
            <img src="https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b52c73d97c954b4aff753b_Serve-your-audience.svg" alt="Presenter speaking to an audience" />
          </div>
          <h2 class="benefit-title">Serve your audience</h2>
          <p class="benefit-description">
            Impress executives and customers by hyper-personalizing your communication 
            to their preferences
          </p>
        </div>
      </div>
      
      <!-- Third Benefit -->
      <div class="benefit-card">
        <div class="card-content">
          <div class="image-container">
            <img src="https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b52c7d44d1b41a21504d5e_Group%20139.svg" alt="Person organizing team collaboration" />
          </div>
          <h2 class="benefit-title">Understand your colleagues</h2>
          <p class="benefit-description">
            Know your teammates better. Learn from their strengths. 
            Collaborate more effectively.
          </p>
        </div>
      </div>
    </div>
  </div>


  <div class="fingerprint-container">
    <h1 class="title">The 8 communication fingerprint types</h1>
    
    <p class="instruction">Click the icons to learn more about each communication fingerprint</p>
    
    <!-- Fingerprint Type Icons -->
    <div class="fingerprint-icons">
      <div 
        v-for="(type, index) in fingerprintTypes" 
        :key="index" 
        class="icon-container"
        @click="selectType(type.id)"
      >
        <h3 class="type-name">{{ type.name }}</h3>
        <div 
          class="icon-circle" 
          :class="{ 'active': selectedType === type.id }"
        >
          <div class="icon" v-html="type.icon"></div>
        </div>
      </div>
    </div>
    
    <!-- Selected Type Details -->
    <div v-if="selectedType" class="type-details">
      <div class="detail-container">
        <div class="detail-icon">
          <div class="icon-circle">
            <div class="icon" v-html="getSelectedTypeIcon()"></div>
          </div>
        </div>
        
        <div class="detail-content">
          <h2 class="detail-title">{{ getSelectedTypePlural() }}</h2>
          <p class="detail-description">{{ getSelectedTypeDescription() }}</p>
          
          <div class="audience-stats">
            <div class="user-avatars">
              <span class="avatar">M</span>
              <span class="avatar">J</span>
              <span class="avatar">K</span>
              <span class="avatar">L</span>
            </div>
            <p class="stats-text">
              +{{ getSelectedTypeAudience() }} audiences across Prezent are {{ getSelectedTypePlural() }}
            </p>
          </div>
        </div>
      </div>
      
      <div class="prezent-branding">
        <div class="video-icon">
          <span class="play-button"></span>
        </div>
      </div>
    </div>
  </div>

  <div class="fingerprint-container">
    <!-- SECTION 1: COMMUNICATION FINGERPRINT -->
    <div class="fingerprint-section">
      <h1 class="main-heading">What a communication fingerprint looks like</h1>
      
      <div class="profile-card">
        <!-- Left side tooltip -->
        <div class="tooltip left-tooltip">
          <div class="tooltip-content">
            Basic details spotlight your profile at a glance.
          </div>
        </div>
        
        <!-- Profile info -->
        <div class="profile-info">
          <div class="profile-header">
            <!-- Profile image -->
            <div class="profile-image-container">
              <div class="profile-image">
                <span>DS</span>
              </div>
              <div class="profile-icon">
                <svg viewBox="0 0 50 50" xmlns="http://www.w3.org/2000/svg">
                  <path d="M25,2 C12.3,2 2,12.3 2,25 C2,37.7 12.3,48 25,48 C37.7,48 48,37.7 48,25 C48,12.3 37.7,2 25,2 Z M34,32 C34,33.1 33.1,34 32,34 L18,34 C16.9,34 16,33.1 16,32 L16,18 C16,16.9 16.9,16 18,16 L32,16 C33.1,16 34,16.9 34,18 L34,32 Z" fill="none" stroke="#0089cc" stroke-width="1.5"></path>
                  <path d="M30,17 L35,23 L30,29 L25,26 L20,29 L17,25" fill="none" stroke="#0089cc" stroke-width="1.5"></path>
                </svg>
              </div>
            </div>
            
            <!-- Name and role -->
            <div class="profile-details">
              <h2 class="profile-name">Divij Sonak <span class="dot">•</span> <span class="role">Performer</span></h2>
              <p class="profile-title">Product Manager • Prezent</p>
              <p class="profile-industry">Healthcare • R&D • Strategy & Operations</p>
              <p class="profile-email">divij.sonak@prezent.ai</p>
            </div>
          </div>
          
          <!-- Right side tooltip -->
          <div class="tooltip down-tooltip">
            <div class="tooltip-content">
              Your fingerprint captures your presentation preferences.
            </div>
          </div>
          
          <!-- Fingerprint description -->
          <div class="fingerprint-description">
            <p><span class="text-bold">Your communication fingerprint is the </span><span class="text-highlight">Performer</span></p>
            <p class="description-text">
              Performers are pragmatic leaders with a bias for action. They process information by analyzing the data and translating it into concrete actionable steps. They appreciate the rich tapestry of bold communication.
            </p>
          </div>
        </div>
      </div>
    </div>
    
    <!-- SECTION 2: PERSONAL PREFERENCES -->
    <div class="preferences-section">
      <h2 class="section-heading">Personal Preferences</h2>
      
      <!-- Tooltip -->
      <div class="tooltip preferences-tooltip">
        <div class="tooltip-content">
          Personal preferences help others tailor slides to your needs.
        </div>
      </div>
      
      <!-- Preferences grid -->
      <div class="preferences-grid">
        <div class="preference-card">
          <div class="preference-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#667080">
              <path d="M19 3H5C3.89 3 3 3.9 3 5v14c0 1.1.89 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 16H5V5h14v14zm-5-7V8h-2v4H8v2h4v2h2v-2h4v-2h-4z"/>
            </svg>
          </div>
          <p class="preference-text">Start with an executive summary</p>
        </div>
        
        <div class="preference-card">
          <div class="preference-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#667080">
              <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 16H5V5h14v14zM7 10h2v7H7zm4-3h2v10h-2zm4 6h2v4h-2z"/>
            </svg>
          </div>
          <p class="preference-text">Label all charts</p>
        </div>
        
        <div class="preference-card">
          <div class="preference-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#667080">
              <path d="M11.8 10.9c-2.27-.59-3-1.2-3-2.15 0-1.09 1.01-1.85 2.7-1.85 1.78 0 2.44.85 2.5 2.1h2.21c-.07-1.72-1.12-3.3-3.21-3.81V3h-3v2.16c-1.94.42-3.5 1.68-3.5 3.61 0 2.31 1.91 3.46 4.7 4.13 2.5.6 3 1.48 3 2.41 0 .69-.49 1.79-2.7 1.79-2.06 0-2.87-.92-2.98-2.1h-2.2c.12 2.19 1.76 3.42 3.68 3.83V21h3v-2.15c1.95-.37 3.5-1.5 3.5-3.55 0-2.84-2.43-3.81-4.7-4.4z"/>
            </svg>
          </div>
          <p class="preference-text">$M instead of $mm</p>
        </div>
        
        <div class="preference-card">
          <div class="preference-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#667080">
              <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm-5-5h10v2H7zm3-3h4v2h-4zm0-3h4v2h-4z"/>
            </svg>
          </div>
          <p class="preference-text">State objective upfront</p>
        </div>
        
        <div class="preference-card">
          <div class="preference-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#667080">
              <path d="M15 1H9v2h6V1zm-4 13h2V8h-2v6zm8.03-6.61l1.42-1.42c-.43-.51-.9-.99-1.41-1.41l-1.42 1.42C16.07 4.74 14.12 4 12 4c-4.97 0-9 4.03-9 9s4.02 9 9 9 9-4.03 9-9c0-2.12-.74-4.07-1.97-5.61zM12 20c-3.87 0-7-3.13-7-7s3.13-7 7-7 7 3.13 7 7-3.13 7-7 7z"/>
            </svg>
          </div>
          <p class="preference-text">3 minutes per slide</p>
        </div>
        
        <div class="preference-card">
          <div class="preference-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#667080">
              <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 16H5V5h14v14zm-7-2h2V7h-4v2h2z"/>
            </svg>
          </div>
          <p class="preference-text">No more than 20 slides</p>
        </div>
        
        <div class="preference-card">
          <div class="preference-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#667080">
              <path d="M4 6H2v14c0 1.1.9 2 2 2h14v-2H4V6zm16-4H8c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h12c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2zm0 14H8V4h12v12zM12 5.5v9l6-4.5z"/>
            </svg>
          </div>
          <p class="preference-text">Tell a visual story</p>
        </div>
      </div>
      
      <!-- Colleague avatars -->
      <div class="colleagues-section">
        <h3 class="section-heading">Personal Preferences</h3>
        <div class="colleagues-avatars">
          <div class="avatar" style="background-color: #29a3d7">
            <span>MM</span>
          </div>
          <div class="avatar" style="background-color: #29a3d7">
            <span>SW</span>
          </div>
          <div class="avatar" style="background-color: #667080">
            <span>HC</span>
          </div>
          <div class="avatar" style="background-color: #f5f5f5; color: #333">
            <span>JD</span>
          </div>
          <div class="avatar avatar-image">
            <img src="https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b7d80cd56ed92372a662b6_avatar.png" alt="Team member">
          </div>
          <span class="colleagues-text">+9 other colleagues are Directors</span>
        </div>
      </div>
    </div>
  </div>

    
    <!-- Main Content -->
    <main class="main-content">
      <!-- Discover Section -->
      <section class="discover-section">
        <h1 class="section-title">Find out which of the 8 communication fingerprint types you are</h1>
        <div class="discover-button-container">
          <button class="btn btn-primary discover-btn">Discover your fingerprint</button>
        </div>
      </section>
      
      <!-- Testimonials Section -->
      <section class="testimonials-section">
        <h2 class="section-title">How the world communicates</h2>
        
        <div class="testimonials-container">
          <!-- Testimonial 1 -->
          <div class="testimonial-card">
            <div class="testimonial-header">
              <div class="testimonial-profile">
                <div class="profile-image-container">
                  <img src="https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b7d80cd56ed92372a662b6_avatar.png" alt="Carla Smith" class="profile-image" />
                </div>
                <div class="profile-icon">
                  <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                    <path d="M50 10 L30 30 L30 70 L50 90 L70 70 L70 30 Z" fill="none" stroke="#0099cc" stroke-width="2" />
                    <path d="M30 50 L70 50" fill="none" stroke="#0099cc" stroke-width="2" />
                  </svg>
                </div>
              </div>
              
              <div class="testimonial-name">
                <h3>Carla Smith <span class="dot">•</span> <span class="type-name">Architect</span></h3>
                <p class="position">Customer Success • Prezent</p>
              </div>
            </div>
            
            <div class="testimonial-content">
              <p>"This is magical! My teammates can personalize everything for me with a few clicks."</p>
            </div>
          </div>
          
          <!-- Testimonial 2 -->
          <div class="testimonial-card">
            <div class="testimonial-header">
              <div class="testimonial-profile">
                <div class="profile-image-container">
                  <img src="https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b7da542e48c7d2a8ceefbb_Ellipse%201.png" alt="Reik Monak" class="profile-image" />
                </div>
                <div class="profile-icon">
                  <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                    <path d="M30 50 L50 30 L70 50 L50 70 Z" fill="none" stroke="#0099cc" stroke-width="2" />
                    <path d="M40 40 L60 60 M60 40 L40 60" fill="none" stroke="#0099cc" stroke-width="2" />
                  </svg>
                </div>
              </div>
              
              <div class="testimonial-name">
                <h3>Reik Monak <span class="dot">•</span> <span class="type-name">Surgeon</span></h3>
                <p class="position">Client Partner • Prezent</p>
              </div>
            </div>
            
            <div class="testimonial-content">
              <p>"I'm amazed how closely this nails down the things I like in a presentation."</p>
            </div>
          </div>
          
          <!-- Testimonial 3 -->
          <div class="testimonial-card">
            <div class="testimonial-header">
              <div class="testimonial-profile">
                <div class="profile-image-container">
                  <img src="https://cdn.prod.website-files.com/6299214533322116e7c4b016/64b7da674c7f046a3ea599c4_Ellipse%201.png" alt="Divij Sonak" class="profile-image" />
                </div>
                <div class="profile-icon">
                  <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                    <path d="M50 20 C30 30, 30 70, 50 80" fill="none" stroke="#0099cc" stroke-width="2" />
                    <path d="M50 20 C60 30, 55 45, 50 50" fill="none" stroke="#0099cc" stroke-width="2" />
                  </svg>
                </div>
              </div>
              
              <div class="testimonial-name">
                <h3>Divij Sonak <span class="dot">•</span> <span class="type-name">Performer</span></h3>
                <p class="position">Product Manager • Prezent</p>
              </div>
            </div>
            
            <div class="testimonial-content">
              <p>"It's amazingly effective! With my fingerprint at their fingertips, the quality of my team's presentations has gone up dramatically."</p>
            </div>
          </div>
        </div>
      </section>
      
      <!-- Learn More Section -->
      <section class="learn-more-section">
        <h2 class="section-title">Find out what other professionals have learned!</h2>
        <div class="discover-button-container">
          <button class="btn btn-primary discover-btn">Discover your fingerprint</button>
        </div>
      </section>
    </main>
  </div>
  <div class="newsletter-container">
    <div class="content-wrapper">
      <h1 class="footer-title">Get the latest from Prezent community</h1>
      <p class="description">
        Join thousands of subscribers who receive our best practices on communication,
        storytelling, presentation design, and more.
      </p>
      <p class="promise">New tips weekly. (No spam, we promise!)</p>
      <div class="form-container">
        <form class="fing-form" @submit.prevent="submitForm">
            <input
              class="fing-field"
              placeholder="Email"
              type="email"
              v-model="email"
              required
            />
            <input
              class="fing-submit"
              type="submit"
              :value="isSubmitting ? 'Submitting...' : 'Subscribe'"
              :disabled="isSubmitting"
            />
          </form>
      </div>
    </div>
    <div class="wave-divider"></div>
  </div>
  <div class="footer-container">
    <!-- Main navigation columns -->
    <div class="footer-navigation">
      <!-- Platform Column -->
      <div class="nav-column">
        <h3 class="column-title">Platform</h3>
        <ul class="link-list">
          <li><a href="#">Create</a></li>
          <li><a href="#">Enable</a></li>
          <li><a href="#">Learn</a></li>
          <li><a href="#">Transform</a></li>
          <li><a href="#">Expert services</a></li>
        </ul>
      </div>

      <!-- Services Column -->
       <div class="column-block">
      <div class="nav-column">
        <h3 class="column-title">Services</h3>
        <ul class="link-list">
          <li><a href="#">Accelerators</a></li>
          <li><a href="#">Zenith Learning Workshops</a></li>
          <li><a href="#">Overnight Presentations</a></li>
        </ul>
      </div>
            <!-- Templates Column -->
            <div class="nav-column">
              <h3 class="column-title">Templates</h3>
              <ul class="link-list">
            <li><a href="#">Corporate Presentation Templates</a></li>
          <li><a href="#">Corporate Slide Templates</a></li>
        </ul>
      </div>

    </div>

          <!-- Resources Column -->
          <div class="nav-column">
        <h3 class="column-title">Resources</h3>
        <ul class="link-list">
          <li><a href="#">Blog</a></li>
          <li><a href="#">Zenpedia</a></li>
          <li><a href="#">Fingerprints</a></li>
          <li><a href="#">Guides</a></li>
          <li><a href="#">Podcast</a></li>
          <li><a href="#">E-Book</a></li>
          <li><a href="#">Case studies</a></li>
          <li><a href="#">Prezent Standard comparison</a></li>
          <li><a href="#">Prezent Premium comparison</a></li>
          <li><a href="#">View demo</a></li>
        </ul>
      </div>
      

      <!-- About Column -->
      <div class="nav-column">
        <h3 class="column-title">About</h3>
        <ul class="link-list">
          <li><a href="#">Story</a></li>
          <li><a href="#">Giving</a></li>
          <li><a href="#">Team</a></li>
          <li><a href="#">Careers</a></li>
          <li><a href="#">News & Press</a></li>
          <li><a href="#">Advisors</a></li>
          <li><a href="#">Prezent for Japan</a></li>
          <li><a href="#">Testimonials</a></li>
        </ul>
      </div>
    </div>

    <!-- Bottom legal and contact section -->
    <div class="footer-bottom">
      <!-- Legal links -->
      <div class="legal-links">
        <a href="#">Contact us</a>
        <a href="#">FAQ</a>
        <a href="#">Cookie policy</a>
        <a href="#">Terms of Service</a>
        <a href="#">Privacy policy</a>
      </div>

      <!-- Contact section -->
      <div class="contact-section">
        <div class="contact-info">
          <a href="tel:+1-440-prezent" class="contact-item">
            <div class="contact-icon phone-icon">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#0089cc">
                <path d="M20 15.5c-1.2 0-2.4-.2-3.6-.6-.3-.1-.7 0-1 .2l-2.2 2.2c-2.8-1.4-5.1-3.8-6.6-6.6l2.2-2.2c.3-.3.4-.7.2-1-.3-1.1-.5-2.3-.5-3.5 0-.6-.4-1-1-1H4c-.6 0-1 .4-1 1 0 9.4 7.6 17 17 17 .6 0 1-.4 1-1v-3.5c0-.6-.4-1-1-1zM5.1 5h1.7c.1.9.3 1.8.5 2.6L5.8 9.1C5.4 7.8 5.1 6.4 5.1 5zM19 18.9c-1.4-.4-2.8-.7-4.1-1.1l1.5-1.5c.8.2 1.7.4 2.6.5V18.9z"/>
              </svg>
            </div>
            <span>+1-440-prezent</span>
          </a>
          <a href="mailto:ask@prezent.ai" class="contact-item">
            <div class="contact-icon email-icon">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#0089cc">
                <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
              </svg>
            </div>
            <span>ask@prezent.ai</span>
          </a>
        </div>

        <div class="social-media">
          <a href="#" class="social-icon youtube">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#0089cc">
              <path d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816zm-10.615 12.816v-8l8 3.993-8 4.007z"/>
            </svg>
          </a>
          <a href="#" class="social-icon linkedin">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="#0089cc">
              <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
            </svg>
          </a>
        </div>

        <div class="copyright">
          <p>2025 © All rights reserved. Prezent, Inc.</p>
        </div>
      </div>

      <!-- Chat Button -->
      <div class="chat-button">
        <button>
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="white">
            <path d="M20 2H4c-1.1 0-2 .9-2 2v18l4-4h14c1.1 0 2-.9 2-2V4c0-1.1-.9-2-2-2z"/>
          </svg>
        </button>
      </div>
    </div>
  </div>
  </div>
</template>


<script>
import './assets/styles.css'

export default {
  name: 'CommunicationFingerprintTypes',
  data() {
    return {
      selectedType: 'architect',
      fingerprintTypes: [
        {
          id: 'architect',
          name: 'Architect',
          icon: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                  <path d="M50 10 L30 30 L30 70 L50 90 L70 70 L70 30 Z" fill="none" stroke="#0099cc" stroke-width="2" />
                  <path d="M30 50 L70 50" fill="none" stroke="#0099cc" stroke-width="2" />
                </svg>`,
          description: 'Architects are innovators energized by the next big thing. They believe in expressing complex ideas with minimalist perfection. They strive for results and are fueled by data.',
          audience: 593
        },
        {
          id: 'director',
          name: 'Director',
          icon: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                  <circle cx="50" cy="35" r="25" fill="none" stroke="#0099cc" stroke-width="2" />
                  <path d="M30 35 L40 45 M60 35 L50 45 M40 55 L50 65 L60 55" fill="none" stroke="#0099cc" stroke-width="2" />
                </svg>`,
          description: 'Directors are pragmatic leaders with a bias for action. They process information by analyzing the data and translating into concrete actionable steps. They appreciate the rich tapestry of bold communication.',
          audience: 425
        },
        {
          id: 'navigator',
          name: 'Navigator',
          icon: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                  <path d="M50 20 L30 40 L40 70 L50 80 L60 70 L70 40 Z" fill="none" stroke="#0099cc" stroke-width="2" />
                  <path d="M40 40 L50 50 L60 40" fill="none" stroke="#0099cc" stroke-width="2" />
                </svg>`,
          description: 'Navigators are confident and bold self-starters. They focus on the key takeaways and appreciate powerful storytelling using vivid images.',
          audience: 5208
        },
        {
          id: 'performer',
          name: 'Performer',
          icon: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                  <path d="M50 20 C30 30, 30 70, 50 80" fill="none" stroke="#0099cc" stroke-width="2" />
                  <path d="M50 20 C60 30, 55 45, 50 50" fill="none" stroke="#0099cc" stroke-width="2" />
                </svg>`,
          description: 'Performers are charismatic presenters who can deliver any message with panache. They like to reach conclusions driven by facts and intuition. They revel in bold visualization of ideas.',
          audience: 870
        },
        {
          id: 'producer',
          name: 'Producer',
          icon: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                  <circle cx="50" cy="50" r="30" fill="none" stroke="#0099cc" stroke-width="2" />
                  <circle cx="35" cy="35" r="5" fill="none" stroke="#0099cc" stroke-width="2" />
                  <circle cx="65" cy="35" r="5" fill="none" stroke="#0099cc" stroke-width="2" />
                  <path d="M40 60 L60 60" fill="none" stroke="#0099cc" stroke-width="2" />
                </svg>`,
          description: 'Producers are risk-takers with clear vision. They believe in the power of good storytelling backed by logic. They avoid anything that distracts them from the main goal.',
          audience: 742
        },
        {
          id: 'scholar',
          name: 'Scholar',
          icon: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                  <circle cx="50" cy="40" r="20" fill="none" stroke="#0099cc" stroke-width="2" />
                  <circle cx="42" cy="35" r="5" fill="none" stroke="#0099cc" stroke-width="2" />
                  <circle cx="58" cy="35" r="5" fill="none" stroke="#0099cc" stroke-width="2" />
                  <path d="M40 50 L50 65 L60 50" fill="none" stroke="#0099cc" stroke-width="2" />
                </svg>`,
          description: 'Scholars are intellectuals seeking to crack the toughest problems. They are highly comfortable with data and appreciate exhaustive analysis to reach any conclusion. They are intrigued by striking visuals.',
          audience: 631
        },
        {
          id: 'scientist',
          name: 'Scientist',
          icon: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                  <path d="M30 60 C40 40, 60 80, 70 30" fill="none" stroke="#0099cc" stroke-width="2" />
                  <circle cx="30" cy="60" r="5" fill="none" stroke="#0099cc" stroke-width="2" />
                  <circle cx="70" cy="30" r="5" fill="none" stroke="#0099cc" stroke-width="2" />
                </svg>`,
          description: 'Scientists are curious learners with an inclination for in-depth problem-solving. They are highly comfortable with data. Simplicity in design helps them keep focus.',
          audience: 489
        },
        {
          id: 'surgeon',
          name: 'Surgeon',
          icon: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
                  <path d="M30 50 L50 30 L70 50 L50 70 Z" fill="none" stroke="#0099cc" stroke-width="2" />
                  <path d="M40 40 L60 60 M60 40 L40 60" fill="none" stroke="#0099cc" stroke-width="2" />
                </svg>`,
          description: 'Surgeons are driven by strong purpose. They strive for logical outcomes backed by wisdom. They believe in succinct communication',
          audience: 356
        }
      ]
    };
  },
  methods: {
    selectType(typeId) {
      this.selectedType = typeId;
    },
    getSelectedType() {
      return this.fingerprintTypes.find(type => type.id === this.selectedType);
    },
    getSelectedTypeIcon() {
      return this.getSelectedType().icon;
    },
    getSelectedTypePlural() {
      const name = this.getSelectedType().name;
      return name + 's';
    },
    getSelectedTypeDescription() {
      return this.getSelectedType().description;
    },
    getSelectedTypeAudience() {
      return this.getSelectedType().audience;
    }
  }
};
</script>
