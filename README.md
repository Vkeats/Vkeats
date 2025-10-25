# Hi, I'm Vincent 👋

## Full-Stack Developer | Theatre Tech | Union Dispatch Software Engineer

I didn't set out to build a production dispatch system. I just kept solving the next problem. Sixteen months later, I'm managing 3,864+ crew members and 17,668+ SMS messages. No roadmap, no plan—just one brick on top of another until it became something real.

**Quick Navigation**: [Featured Project](#featured-project-the-board) • [Current Work](#current-projects) • [Journey](#development-journey) • [Skills](#technical-expertise) • [Philosophy](#philosophy)

---

## Featured Project: The Board

**Production-grade crew dispatch system** managing theatre crew scheduling, SMS communication, and worker assignments for union locals. Built while working as a union dispatcher to solve real-world workflow challenges.

### Production Stats
- **3,864 workers** actively managed
- **17,668+ SMS messages** sent and processed
- **77 shows/events** with 598 positions dispatched
- **84,544+ database records** in production
- **141 REST API endpoints** with 100% authentication coverage
- **Real-time WebSocket updates** for live coordination

### Tech Stack
```
Frontend:   Next.js 15 • React 19 • TypeScript • Tailwind CSS • DaisyUI
Backend:    Next.js API Routes • Service Layer Pattern • WebSocket
Database:   SQLite (Better-SQLite3) • 49 tables • 56 migrations
Auth:       NextAuth.js • Session-based • Rate limiting
SMS:        Multi-provider (Twilio/YakChat/TextMagic)
Testing:    Jest • Playwright • Integration tests
```

### Key Features
- **Intelligent Dispatch**: Seniority-based automatic assignment with conflict detection
- **SMS Integration**: Pattern-based response parsing, batch processing, real-time monitoring
- **Union Policy Engine**: Configurable strategies for different union scenarios
- **Advanced Analytics**: Structured logging with correlation IDs and performance metrics
- **Security First**: 100% API protection, rate limiting, failed login tracking

**[Read the Full Development Journey](https://github.com/Vkeats/Vkeats/blob/master/DEVELOPMENT_JOURNEY.md)** - From learning to code to production in 16 months

---

## Current Projects

### [crew-caller](https://github.com/Vkeats/crew-caller) - Production System
**Status**: Active Production | **Created**: June 2024

The current production dispatch system serving union locals. Handles all real-world crew scheduling, SMS communication, and assignment management.

**Highlights**:
- 96 React components with specialized "app" components
- 66 library modules with 462 exports
- Comprehensive documentation system
- PM2/Docker deployment ready

### [the-board](https://github.com/Vkeats/the-board) - Next Generation
**Status**: In Active Development | **Created**: October 2024

Next-generation platform with cloud-native architecture and enhanced features.

**Planned Improvements**:
- PostgreSQL for production-scale concurrent access
- AI-powered SMS response parsing (vs regex)
- Mobile app for workers
- Advanced analytics and reporting
- Enhanced real-time collaboration features

---

## Development Journey

### From Zero to Production in 16 Months

```
Phase 1: Learning Fundamentals (Dec 2023 - Jun 2024)
├─ learning: Basic programming concepts
└─ Dungeon-Crawler-Project: First complete project

Phase 2: Early Prototypes (Mar 2024)
├─ Appv2: Early web stack exploration
├─ Staff-Manager: First crew management system
└─ Union-Local: Union workflow exploration

Phase 3: Feature Development (Feb - Mar 2024)
├─ Algorithm: Intelligent worker assignment algorithms
└─ iatse-dispatch: First dispatch system with SMS

Phase 4: Integration & Consolidation (Jun - Jul 2024)
├─ UnionManager: Comprehensive platform integration
└─ CallSteward-CSV-Wizard: Legacy data migration tools

Phase 5: Production (Jun 2024 - Present)
└─ crew-caller: Production-ready system with 84k+ records

Phase 6: Next Generation (Oct 2024 - Future)
└─ the-board: Cloud-native PostgreSQL platform
```

**What Actually Happened**:
- Each repository solved an immediate problem, not a planned phase
- Production users taught me what actually mattered (not documentation)
- I discovered patterns by building, not by designing upfront
- Tests came when things broke enough times to hurt
- The "architecture" emerged from solving real problems

[**Read the complete story →**](https://github.com/Vkeats/Vkeats/blob/master/DEVELOPMENT_JOURNEY.md)

---

## Technical Expertise

### Languages & Frameworks
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)

### Databases & Tools
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

### Specialized Skills
- **Real-time Systems**: WebSocket architecture, live updates, concurrent operations
- **SMS Integration**: Multi-provider management, pattern parsing, batch processing
- **API Design**: RESTful architecture, rate limiting, authentication, error handling
- **Database Design**: Schema design, migrations, performance optimization
- **Production DevOps**: PM2, Docker, Railway deployment, monitoring

---

## Highlights & Achievements

### Production Impact
- Deployed and actively managing **3,864 theatre crew members**
- Processing **17,000+ SMS messages** with multi-provider reliability
- **100% API security coverage** across 141 endpoints
- Real-time dispatch coordination serving multiple union locals

### Technical Achievements
- Built comprehensive service layer architecture from scratch
- Implemented production-grade security with rate limiting and session management
- Created multi-provider SMS system with automatic failover
- Designed WebSocket system for real-time collaborative dispatch
- Established comprehensive testing suite (Jest + Playwright + Integration)

### Code Quality
- Wrote **7,000+ lines of documentation**
- Maintained **TypeScript strict mode** across entire codebase
- **56 database migrations** with full rollback support
- Structured logging with correlation IDs for debugging

---

## What I'm Working On

- Migrating **crew-caller** → **the-board**: PostgreSQL migration (Phase 1 of 6-phase plan)
- Implementing AI-powered SMS response parsing to replace regex patterns
- Building React Native mobile app for workers
- Creating advanced analytics dashboards
- Designing third-party integration APIs

---

## Connect With Me

- **GitHub**: You're already here!
- **Email**: Available on request
- **Industry**: Theatre Technology & Union Dispatch Systems

---

## Philosophy

> "Modern technology should enhance traditional workflows, not replace them. The best software respects the domain expertise of its users while automating the tedious parts."

I believe in:
- **Incremental iteration** over big rewrites
- **Production feedback** over theoretical perfection
- **Documentation** as a force multiplier
- **Testing** as a requirement, not an afterthought
- **User needs** over technical ego

---

## Documentation Philosophy

Every project includes:
- Comprehensive README with quick start guides
- Architecture documentation explaining design decisions
- Development guides for contributor onboarding
- API reference with examples
- Testing documentation and strategies

**Example**: The crew-caller project includes 8 major documentation files covering everything from deployment to development workflows, with comprehensive API references and architecture guides.

---

<div align="center">

**Building the future of theatre crew management, one commit at a time**

</div>
