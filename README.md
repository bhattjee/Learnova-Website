# Learnova - All-in-One Learning Platform

<div align="center">

![Learnova Logo](images/logo.png)

**Limitless Learning. Limitless Growth.**

A modern, responsive learning management system designed for learners, instructors, and administrators.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://www.w3.org/html/)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://www.w3.org/Style/CSS/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://www.javascript.com/)

</div>

---

## Overview

Learnova is a comprehensive learning platform that unifies the educational experience for three key user roles:

- **Learners**: Discover courses, track progress, maintain learning streaks, and earn certifications
- **Instructors**: Create and manage courses, analyze learner data, and scale their educational impact
- **Administrators**: Oversee platform operations, manage users, and access comprehensive reporting

## Key Features

### For Learners
- 🎯 **Course Discovery**: Browse and enroll in 180+ curated programs
- 📊 **Progress Tracking**: Real-time dashboards with completion metrics
- 🔥 **Learning Streaks**: Gamified daily engagement tracking
- 🏆 **Rank & Badge System**: Level up as you master new skills
- 📱 **Fully Responsive**: Learn on any device, anywhere

### For Instructors
- 📝 **Course Management**: Create and organize course content with ease
- 📈 **Analytics Dashboard**: Track learner engagement and completion rates
- 🎬 **Multi-format Lessons**: Support for video, documents, and images
- 📋 **Kanban-style Workflow**: Visual course organization and management
- 🔄 **Real-time Updates**: Instant feedback on learner progress

### For Administrators
- 👥 **User Management**: Comprehensive oversight of all platform users
- 📊 **Advanced Reporting**: Deep insights into platform performance
- 🔐 **Role-based Access**: Granular permission controls
- 🚨 **Alert System**: Urgent review notifications and action items

## Architecture

### Current Implementation
- **Frontend**: Static HTML5 pages with Tailwind CSS
- **Styling**: Tailwind CSS via CDN with custom configurations
- **Icons**: Lucide Icons library
- **JavaScript**: Vanilla JS for interactivity and routing
- **Design System**: Custom bento-grid layouts with responsive breakpoints

### Planned Tech Stack
See the [Tech Plan](Techplan/learnova_full_tech_plan.html) for detailed architecture:

- **Frontend**: React 18 + Vite
- **UI Components**: Tailwind CSS + shadcn/ui
- **State Management**: Zustand + TanStack Query
- **Backend**: Python FastAPI
- **Database**: PostgreSQL with SQLAlchemy ORM
- **Authentication**: JWT + bcrypt
- **File Storage**: Cloudflare R2
- **Email Service**: Resend
- **Deployment**: Vercel (frontend) + Railway (backend)

## Project Structure

```
Learnova-Website/
├── css/
│   └── site-responsive.css          # Shared responsive baseline styles
├── images/
│   ├── logo.png                     # Platform logo (PNG)
│   └── logo.svg                     # Platform logo (SVG)
├── js/
│   ├── app-links.js                 # SPA routing integration
│   └── role-tour.js                 # Interactive tour functionality
├── screenshots/
│   ├── Admin-Images/                # Admin interface screenshots
│   ├── Blog-Images/                 # Blog post images
│   ├── Instructor-Images/           # Instructor interface screenshots
│   ├── Learner-Images/              # Learner interface screenshots
│   ├── loginpage.png                # Login page screenshot
│   └── signuppage.png               # Signup page screenshot
├── Techplan/
│   └── learnova_full_tech_plan.html # Comprehensive technical documentation
├── about.html                       # About Us page
├── admin-dashboard.html             # Admin dashboard interface
├── admin-editor.html                # Course editor interface
├── admin-reporting.html             # Reporting and analytics interface
├── blog.html                        # Blog and insights page
├── course-detail.html               # Course detail view
├── index.html                       # Landing page
├── player.html                      # Video/content player
├── privacy.html                     # Privacy policy
├── quiz.html                        # Quiz interface
└── tour.html                        # Interactive product tour
```

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- No build tools required for current static version
- For planned React version: Node.js 18+ and npm/yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/bhattjee/Learnova-Website.git
   cd Learnova-Website
   ```

2. **Open the project**
   - Simply open `index.html` in your web browser
   - Or use a local server:
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Using Node.js (http-server)
     npx http-server
     ```

3. **Explore the platform**
   - Visit `http://localhost:8000` (or your chosen port)
   - Navigate through different user roles using the tour feature
   - Check the tech plan for implementation details

## Design System

### Color Palette
```css
--primary: #1D4ED8        /* Main brand blue */
--dark-gray: #464749      /* Text and UI elements */
--light-gray: #C5CAD3     /* Borders and subtle elements */
--secondary-red: #EF4444  /* Alerts and urgent items */
--accent-orange: #F5AA29  /* Streaks and achievements */
--accent-purple: #7632EC  /* Analytics and insights */
--accent-green: #058E61   /* Success states and certifications */
```

### Typography
- **Font Family**: Source Sans Pro
- **Weights**: 300 (Light), 400 (Regular), 600 (Semi-bold), 700 (Bold)
- **Google Fonts**: Integrated via CDN

### Responsive Breakpoints
- **Mobile**: < 640px
- **Tablet**: 640px - 1024px
- **Desktop**: > 1024px

## Pages Overview

| Page | Description | Key Features |
|------|-------------|--------------|
| `index.html` | Landing page | Hero section, learner hub, instructor studio, FAQ |
| `tour.html` | Product tour | Role-based interactive walkthroughs |
| `about.html` | About us | Company mission and values |
| `blog.html` | Blog & insights | Articles, podcasts, featured stories |
| `course-detail.html` | Course view | Course information, instructor details |
| `player.html` | Content player | Video/document/image viewer |
| `quiz.html` | Quiz interface | Interactive assessments |
| `admin-dashboard.html` | Admin panel | User management, overview |
| `admin-editor.html` | Course editor | Content creation tools |
| `admin-reporting.html` | Analytics | Data visualization and reports |
| `privacy.html` | Privacy policy | Legal information |

## Customization

### Updating Branding
1. Replace `images/logo.png` and `images/logo.svg` with your logo
2. Update color variables in Tailwind config (in each HTML file)
3. Modify the brand name in navigation and footer sections

### Modifying Content
- All text content is directly editable in HTML files
- Blog articles are stored in the `blogData` object in `blog.html`
- Tour content is managed in `tour.html`

### Adding New Pages
1. Create a new HTML file in the root directory
2. Include the shared CSS: `<link rel="stylesheet" href="css/site-responsive.css" />`
3. Add Tailwind CSS and Lucide Icons CDNs
4. Update navigation links across existing pages

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Contact

For questions, suggestions, or collaboration opportunities:
- Open an issue on GitHub
- Email: [Replace with your contact email]

## Acknowledgments

- **Tailwind CSS** for the utility-first CSS framework
- **Lucide Icons** for the beautiful icon set
- **Google Fonts** for Source Sans Pro typography
- **Unsplash** for placeholder images

## Roadmap

- [ ] Migrate to React + Vite architecture
- [ ] Implement FastAPI backend
- [ ] Set up PostgreSQL database
- [ ] Add user authentication
- [ ] Integrate file storage (Cloudflare R2)
- [ ] Implement email notifications (Resend)
- [ ] Deploy to production (Vercel + Railway)

---

<div align="center">

**Built with ❤️ for the future of education**

[⬆ Back to Top](#learnova---all-in-one-learning-platform)

</div>
