# The Board: Development Journey

**From Learning to Production** - A chronicle of building a theatre crew dispatch system for IATSE unions

---

## Executive Summary

**The Honest Version**: I didn't plan any of this. I just kept solving the next immediate problem in front of me. Sixteen months of "one more brick" turned into a production system managing 3,864 workers.

**Timeline**: Dec 2023 - Oct 2024 (16 months)
**Pattern**: Problem → Ugly solution → Slightly less ugly solution → Repeat
**Repositories**: 11 failed experiments that taught me what actually works
**Current State**: A system that actually works in production (shocking)
**Key Metrics**: 84,544+ DB records, 17,668+ SMS processed, 141 API endpoints

**This isn't a story about planning. It's about stumbling forward until something clicked.**

---

## Overview

This document traces the evolution of **The Board** from initial concept to production-ready system, spanning 11 repositories and 16+ months of development (December 2023 - October 2024). What started as a learning project evolved into a comprehensive theatre crew dispatching system processing thousands of SMS messages and managing hundreds of worker assignments.

---

## Timeline & Evolution

### Phase 1: Foundation & Learning (Dec 2023 - Jun 2024)

#### **learning** (Dec 2023)
*"I'm learning to code here"*

**Status**: Archived
**Purpose**: Initial coding education and experimentation
**Key Learnings**:
- Basic programming fundamentals
- Early explorations of web development
- Foundation for future projects

#### **Dungeon-Crawler-Project** (Jun 2024)
**Status**: Archived
**Purpose**: First complete project - game development exercise
**Key Learnings**:
- Project structure and organization
- State management basics
- Algorithm development

---

### Phase 2: Early Prototypes (Mar 2024)

#### **Appv2** (Mar 2024)
**Status**: Archived
**Technologies**: Early web stack exploration
**Purpose**: Second generation application prototype
**Key Developments**:
- Initial exploration of union crew management concepts
- Database modeling experiments
- Early UI/UX patterns

#### **Staff-Manager** (Mar 2024)
**Status**: Archived
**Purpose**: First attempt at crew management system
**Key Features**:
- Basic staff database
- Simple assignment tracking
- Foundation for roster management concepts

#### **Union-Local** (Mar 2024)
**Status**: Archived
**Purpose**: Union-specific workflow exploration
**Key Insights**:
- Understanding IATSE union rules
- Seniority-based assignment concepts
- Worker qualification tracking

---

### Phase 3: Feature Development & Iteration (Feb - Mar 2024)

#### **Algorithm** (Feb - Mar 2024)
*"Union Worker Algorithm App"*

**Status**: Archived
**Purpose**: Intelligent worker assignment algorithms
**Major Innovations**:
- Seniority-based ranking algorithms
- Skill matching logic
- Conflict detection systems
- Availability tracking

**Why It Matters**: This repository established the core business logic that powers automatic worker assignment, a critical feature that survived into the final product.

#### **iatse-dispatch** (Mar 2024)
**Status**: Archived
**Purpose**: First dispatch-focused system
**Breakthrough Features**:
- SMS integration concept
- Dispatch workflow design
- Job position management

---

### Phase 4: Integration & Consolidation (Jun - Jul 2024)

#### **UnionManager** (Jun 2024)
**Status**: Archived
**Purpose**: Comprehensive union management platform
**Key Integrations**:
- Combined worker management + dispatch
- Enhanced SMS workflow
- Database schema maturation
- Multi-job support

#### **CallSteward-CSV-Wizard** (Jul 2024)
**Status**: Archived
**Purpose**: Data migration and import tools
**Critical Features**:
- CSV import wizard for CallSteward legacy data
- Skills list parsing
- Worker database import
- Position template system

**Legacy Integration**: This tool enabled migration from CallSteward (existing system) to The Board, a critical requirement for production adoption.

---

### Phase 5: Production Development (Jun 2024 - Present)

#### **crew-caller** (Jun 2024 - Present)
*"does my job for me"* - **CURRENT PRODUCTION SYSTEM**

**Status**: Active Production
**Created**: June 28, 2024
**Last Updated**: October 24, 2024 (Active development)

**Tech Stack**:
- **Frontend**: Next.js 15, React 19, TypeScript, Tailwind CSS + DaisyUI
- **Backend**: 141 API routes with service layer pattern
- **Database**: SQLite (Better-SQLite3) - 49 tables, 84,544+ records
- **Real-time**: WebSocket system for live updates
- **SMS**: Multi-provider (Twilio/YakChat/TextMagic)
- **Auth**: NextAuth.js with 100% API coverage

**Production Statistics**:
- **Workers**: 3,864 crew members
- **Jobs**: 77 shows/events
- **Positions**: 598 individual calls
- **Assignments**: 319 active assignments
- **SMS Logs**: 17,668 messages sent
- **Worker Skills**: 58,510 qualification records
- **Database Size**: 84,544+ total records across 49 tables

**Key Features**:
1. **Advanced Dispatch System**
   - Unified Roster App with tabbed interface
   - Position Heatmap Grid for visual assignment tracking
   - Intelligent conflict resolution
   - Real-time response analytics

2. **SMS Integration**
   - Automated crew communication
   - Pattern-based response parsing (regex)
   - Batch processing with rate limiting
   - Real-time monitoring dashboard
   - Structured logging with correlation IDs

3. **Union Policy Engine**
   - Configurable policy strategies
   - Seniority-based automatic assignment
   - Conflict detection and override system
   - Vacation/medical tracking

4. **Security & Compliance**
   - 100% API protection (141/141 endpoints)
   - Rate limiting on all routes
   - Failed login tracking
   - Webhook validation
   - Session-based authentication

**Development Highlights**:
- 56 database migrations
- 96 React components
- 66 library modules with 462 exports
- Comprehensive test suite (Jest + Playwright)
- Full documentation system

**Why This Succeeded**: crew-caller represents the culmination of all previous learning, combining:
- Algorithm's intelligent assignment logic
- CallSteward-CSV-Wizard's import capabilities
- UnionManager's comprehensive feature set
- Real-world production requirements and feedback
- Modern tech stack and best practices

---

### Phase 6: Next Generation Architecture (Oct 2024 - Future)

#### **the-board** (Oct 2024 - Future)
*"IATSE 118 Crew Dispatch System - Intelligent one-click dispatch"*

**Status**: In Development (Production Migration Target)
**Created**: October 21, 2024
**Purpose**: Next-generation production system

**Tech Stack Evolution**:
- **Database**: SQLite → **PostgreSQL** (Production-grade scaling)
- **Architecture**: Monolithic → **Modular microservices**
- **Deployment**: Self-hosted → **Cloud-native (Railway/Vercel)**
- **Real-time**: WebSocket → **Enhanced real-time features**

**Planned Improvements**:
1. **Scalability**
   - PostgreSQL for better concurrent access
   - Horizontal scaling capabilities
   - Cloud-native deployment

2. **Enhanced Features**
   - AI-powered response parsing (vs regex)
   - Advanced analytics and reporting
   - Mobile app for workers
   - Multi-venue support

3. **Architecture**
   - Cleaner separation of concerns
   - API-first design
   - Enhanced caching layer
   - Improved WebSocket architecture

4. **Developer Experience**
   - Better testing infrastructure
   - CI/CD pipeline
   - Automated deployment
   - Enhanced monitoring

**Migration Strategy**: See [MIGRATION_PLAN.md](#migration-plan) below.

---

## Architecture Evolution

### Database Journey
```
Learning Phase:        No database → In-memory state
Early Prototypes:      SQLite basics → Simple schemas
Algorithm Phase:       Complex relationships → 38,000+ skill records
UnionManager:          35+ tables → Migration system
crew-caller:           49 tables → 84,544+ records → Production-grade
the-board:             PostgreSQL → Cloud-scale → Enhanced schemas
```

### Feature Evolution
```
Staff-Manager:         Basic roster
iatse-dispatch:        + SMS integration
Algorithm:             + Intelligent assignment
UnionManager:          + Multi-job support
CallSteward-CSV:       + Data migration tools
crew-caller:           + Real-time updates + Advanced analytics
the-board:             + AI parsing + Mobile app + Cloud deployment
```

### Technology Stack Evolution
```
Learning:              Basic HTML/CSS/JS
Early Prototypes:      React basics
Algorithm:             TypeScript + Advanced state management
UnionManager:          Next.js + API routes
crew-caller:           Next.js 15 + React 19 + Full stack
the-board:             + PostgreSQL + Cloud-native + Microservices
```

### Scale Evolution by Numbers

| Metric | Algorithm (Mar '24) | UnionManager (Jun '24) | crew-caller (Oct '24) | the-board (Target) |
|--------|---------------------|------------------------|----------------------|-------------------|
| Workers | ~100 | ~500 | 3,864 | 10,000+ |
| Tables | 10 | 35 | 49 | 55+ |
| API Endpoints | 0 | ~50 | 141 | 200+ |
| SMS Sent | 0 | ~1,000 | 17,668+ | 100,000+ |
| Components | ~10 | ~40 | 96 | 120+ |
| Test Coverage | None | Basic | Comprehensive | Enhanced |
| Deployment | Local | Local | PM2/Docker | Cloud-native |

---

## Key Learnings & Insights

### What Worked
1. **Incremental Development**: Each repository built on previous learnings
2. **Real-World Testing**: Production use informed feature priorities
3. **Modern Stack**: Next.js 15 + TypeScript provided solid foundation
4. **Modular Architecture**: Service layer pattern enabled clean code organization
5. **Comprehensive Documentation**: Saved time during refactoring and onboarding

### Challenges Overcome
1. **SMS Provider Reliability**: Built multi-provider system to handle failures
2. **Concurrent Updates**: WebSocket system solved real-time coordination
3. **Complex Union Rules**: Strategy pattern enabled flexible policy management
4. **Data Migration**: CSV import wizard solved CallSteward migration
5. **Performance at Scale**: SQLite WAL mode + Better-SQLite3 handled production load

### Technical Debt Addressed
1. **Authentication**: Evolved from basic auth → NextAuth.js with 100% coverage
2. **Error Handling**: Centralized error handling across all API routes
3. **Rate Limiting**: Comprehensive rate limiting on all endpoints
4. **Logging**: Structured JSON logging with correlation IDs
5. **Testing**: Comprehensive test suite (Jest + Playwright + Integration)

---

## Lessons Learned: Advice for Others

### For Self-Taught Developers
1. **You don't need to know what you're building**: I had no idea this would become a production system. Just solve today's problem.
2. **Real problems > tutorials**: I learned more breaking production than from any course
3. **Don't wait for "ready"**: I shipped broken code and fixed it when users complained
4. **Copy what works**: I stole patterns from Next.js docs, Stack Overflow, and anywhere else that had answers
5. **Ugly code that works beats perfect code that doesn't**: Refactor when pain exceeds pride

### For Theatre Tech (Or Any Domain Expert Learning to Code)
1. **Your domain knowledge is the cheat code**: I understood dispatch workflows better than I understood JavaScript—that mattered more
2. **Build for yourself first**: I was my own first user. That feedback loop was invaluable
3. **Users forgive bad UI if it solves their problem**: My first interfaces were terrible. Nobody cared because it saved them hours

### What Actually Happened (Not What I Planned)
1. **No tests until things broke enough to hurt**: Tests came after the third time I broke SMS in production
2. **Documentation came from forgetting how my own code worked**: I documented when I got confused by code I wrote last month
3. **"Architecture" = refactoring the same mess three times**: The service layer pattern emerged from copy-pasting the same code too many times
4. **TypeScript saved me after JavaScript broke me**: I added TypeScript after JavaScript allowed too many stupid bugs
5. **The 1,000 SMS incident taught me rate limiting**: Real mistakes teach better than best practices

### What I'd Still Do Differently
1. **Actually, I'd probably do it exactly the same**: The mess taught me more than a clean path would have
2. **Maybe fewer repositories**: But each one taught me something I needed to learn
3. **Okay fine, tests earlier**: But I wouldn't have appreciated them without the pain

---

## Repository Archive Strategy

### Recommended Actions

#### **Archive** (Preserve history, mark read-only)
- ✅ `learning` - Educational value, shows learning journey
- ✅ `Dungeon-Crawler-Project` - First complete project milestone
- ✅ `Appv2` - Early prototype, architectural learning
- ✅ `Staff-Manager` - First crew management attempt
- ✅ `Union-Local` - Union workflow exploration
- ✅ `iatse-dispatch` - First dispatch system
- ✅ `Algorithm` - Core algorithm development
- ✅ `UnionManager` - Feature consolidation phase
- ✅ `CallSteward-CSV-Wizard` - Data migration tool (completed)

#### **Active Development**
- 🚀 `crew-caller` - Current production system
- 🚀 `the-board` - Next-generation production system

### Archive Commands
```bash
# Archive old repositories (preserve history)
gh repo archive Vkeats/learning
gh repo archive Vkeats/Dungeon-Crawler-Project
gh repo archive Vkeats/Appv2
gh repo archive Vkeats/Staff-Manager
gh repo archive Vkeats/Union-Local
gh repo archive Vkeats/iatse-dispatch
gh repo archive Vkeats/Algorithm
gh repo archive Vkeats/UnionManager
gh repo archive Vkeats/CallSteward-CSV-Wizard
```

### Update Repository Descriptions
```bash
# Add context to repository descriptions
gh repo edit Vkeats/learning --description "Phase 1: Learning fundamentals (Dec 2023) - See DEVELOPMENT_JOURNEY.md in crew-caller"
gh repo edit Vkeats/Dungeon-Crawler-Project --description "Phase 1: First complete project (Jun 2024)"
gh repo edit Vkeats/Appv2 --description "Phase 2: Early prototype (Mar 2024)"
gh repo edit Vkeats/Staff-Manager --description "Phase 2: First crew management system (Mar 2024)"
gh repo edit Vkeats/Union-Local --description "Phase 2: Union workflow exploration (Mar 2024)"
gh repo edit Vkeats/Algorithm --description "Phase 3: Intelligent worker assignment algorithms (Feb-Mar 2024)"
gh repo edit Vkeats/iatse-dispatch --description "Phase 3: First dispatch system with SMS (Mar 2024)"
gh repo edit Vkeats/UnionManager --description "Phase 4: Comprehensive integration (Jun 2024)"
gh repo edit Vkeats/CallSteward-CSV-Wizard --description "Phase 4: Legacy data migration tool (Jul 2024)"
gh repo edit Vkeats/crew-caller --description "Phase 5: Production system - IATSE crew dispatch (Jun 2024 - Active)"
gh repo edit Vkeats/the-board --description "Phase 6: Next-gen production system - Cloud-native PostgreSQL (Oct 2024 - In Development)"
```

---

## What's Still Missing (And Why That's OK)

**Current Gaps in crew-caller**:
- **No CI/CD pipeline**: Manual deployments via PM2 work for current scale
- **Limited automated testing for SMS flows**: Hard to test external SMS provider APIs reliably
- **No proper staging environment**: Production database is carefully managed, but no separate staging instance
- **Minimal error alerting**: PM2 logs + manual checking instead of automated monitoring/alerts
- **No database backups automation**: Manual backups work, but not automated
- **Limited performance monitoring**: Basic logging without APM tools

**Why This Is Acceptable**:
These gaps are acceptable trade-offs for the current scale and single-developer context. The system is stable, serves real users reliably, and manual processes work at this scale. Perfect is the enemy of shipped—these gaps didn't prevent production deployment or reliable operation.

**Addressed in the-board Migration**:
- **Phase 1**: CI/CD pipeline + staging environment setup
- **Phase 1**: Automated database backups (PostgreSQL on Railway/Supabase)
- **Phase 2**: Enhanced monitoring and alerting infrastructure
- **Phase 3**: Improved test coverage including SMS mocking strategies
- **Phase 4**: APM integration for performance monitoring

This honest assessment shows growth mindset and technical maturity—knowing what's missing, why it's acceptable now, and planning to address it systematically.

---

## Migration Plan: crew-caller → the-board

### Overview
The migration from crew-caller to the-board represents a strategic evolution rather than a complete rewrite. The goal is to maintain all core functionality while modernizing infrastructure for better scalability and performance.

### Migration Status Dashboard

| Phase | Status | Timeline | Completion |
|-------|--------|----------|------------|
| Phase 1: Infrastructure | ⚪ Not Started | Weeks 1-2 | 0% |
| Phase 2: Database | ⚪ Not Started | Weeks 3-4 | 0% |
| Phase 3: Code Adaptation | ⚪ Not Started | Weeks 5-7 | 0% |
| Phase 4: Feature Parity | ⚪ Not Started | Weeks 8-10 | 0% |
| Phase 5: Parallel Operation | ⚪ Not Started | Weeks 11-12 | 0% |
| Phase 6: Cutover | ⚪ Not Started | Week 13 | 0% |

**Legend**: 🟢 Complete | 🟡 In Progress | 🔴 Blocked | ⚪ Not Started

### Migration Phases

#### Phase 1: Infrastructure Setup (Weeks 1-2)
**Objectives**:
- Set up PostgreSQL database on Railway/Supabase
- Configure cloud deployment pipeline
- Establish CI/CD automation
- Set up monitoring and logging infrastructure

**Deliverables**:
- [ ] PostgreSQL instance provisioned
- [ ] Database schema migrated and tested
- [ ] Deployment pipeline configured
- [ ] Environment variables secured
- [ ] Monitoring dashboards created

#### Phase 2: Database Migration (Weeks 3-4)
**Objectives**:
- Migrate SQLite schema to PostgreSQL
- Adapt 56 migrations for PostgreSQL compatibility
- Create data migration scripts
- Validate data integrity

**Key Considerations**:
- SQLite-specific features (e.g., `AUTOINCREMENT` → `SERIAL`)
- Date/time handling differences
- Transaction isolation levels
- Full-text search migration

**Deliverables**:
- [ ] All 49 tables migrated to PostgreSQL
- [ ] Migration scripts tested and validated
- [ ] Data integrity verification complete
- [ ] Rollback procedures documented

#### Phase 3: Code Adaptation (Weeks 5-7)
**Objectives**:
- Replace Better-SQLite3 with node-postgres/Prisma
- Adapt database access layer
- Update API routes for async operations
- Maintain backward compatibility

**Changes Required**:
```typescript
// Before (crew-caller - synchronous)
const db = getDatabase()
const workers = db.prepare('SELECT * FROM workers').all()

// After (the-board - asynchronous)
const workers = await db.query('SELECT * FROM workers')
```

**Deliverables**:
- [ ] Database layer refactored for async/await
- [ ] All 141 API routes updated
- [ ] Service layer adapted
- [ ] Unit tests passing

#### Phase 4: Feature Parity (Weeks 8-10)
**Objectives**:
- Verify all crew-caller features work in the-board
- Enhanced real-time features
- Improved SMS handling
- Enhanced analytics

**Testing Focus**:
- All 96 components render correctly
- WebSocket functionality maintained
- SMS batch processing working
- Assignment algorithms accurate
- Import wizards functional

**Deliverables**:
- [ ] Feature checklist 100% complete
- [ ] E2E tests passing
- [ ] Performance benchmarks met
- [ ] User acceptance testing complete

#### Phase 5: Parallel Operation (Weeks 11-12)
**Objectives**:
- Run both systems in parallel
- Shadow production traffic
- Validate data consistency
- Monitor performance

**Monitoring**:
- Response time comparison
- Error rate tracking
- Data sync verification
- User experience feedback

**Deliverables**:
- [ ] Systems running in parallel
- [ ] Performance metrics collected
- [ ] Bug fixes deployed
- [ ] Confidence established

#### Phase 6: Migration & Cutover (Week 13)
**Objectives**:
- Final data synchronization
- DNS/traffic cutover
- Monitor closely for issues
- Maintain crew-caller as fallback

**Cutover Plan**:
1. Announce maintenance window
2. Final data sync from crew-caller
3. Switch traffic to the-board
4. Monitor for 24-48 hours
5. Verify all operations
6. Keep crew-caller ready for rollback

**Deliverables**:
- [ ] Production cutover complete
- [ ] All users migrated
- [ ] System stable for 48+ hours
- [ ] crew-caller archived as backup

### Risk Mitigation

#### High-Risk Areas
1. **Database Migration**
   - Risk: Data loss or corruption
   - Mitigation: Multiple backups, dry-run migrations, validation scripts

2. **SMS Provider Integration**
   - Risk: Message delivery failures during transition
   - Mitigation: Maintain dual-write during parallel phase

3. **Real-time Updates**
   - Risk: WebSocket connection issues
   - Mitigation: Enhanced error handling, automatic reconnection

4. **Performance Regression**
   - Risk: Slower response times with PostgreSQL
   - Mitigation: Connection pooling, query optimization, caching

#### Rollback Procedures
- **Immediate Rollback**: DNS switch back to crew-caller (< 5 minutes)
- **Data Rollback**: Restore from last backup (< 30 minutes)
- **Code Rollback**: Revert deployment via CI/CD (< 10 minutes)

### Success Metrics
- [ ] Zero data loss during migration
- [ ] 99.9% uptime during transition
- [ ] Response times < 200ms (p95)
- [ ] All 141 API endpoints functional
- [ ] SMS delivery rate maintained
- [ ] User satisfaction scores maintained

### Post-Migration Enhancements

Once migration is stable, implement new features:

1. **AI-Powered Enhancements**
   - NLP-based SMS response parsing (replace regex)
   - Intelligent assignment suggestions
   - Predictive analytics

2. **Mobile Application**
   - React Native worker app
   - Push notifications
   - Offline support

3. **Advanced Analytics**
   - Custom reporting dashboards
   - Historical trend analysis
   - Workforce optimization insights

4. **Integration APIs**
   - Payroll system integration
   - Calendar sync
   - Third-party dispatch tools

---

## Conclusion: The Accidental Architecture

Here's the truth: I didn't build a production dispatch system. I just refused to stop solving problems.

### What Really Happened

I started with "I need to learn to code." Then it became "I need to track crew members." Then "I need to send SMS." Then "I need to handle responses." Each time, I built the dumbest thing that could possibly work.

**Eleven repositories later**, those dumb things had turned into something that actually works. Not because I'm clever—because I kept showing up and refused to let problems stay unsolved.

### The Pattern That Emerged

Looking back (because I sure wasn't looking forward), there was a pattern:
1. **Face a problem** that annoyed me enough
2. **Build something ugly** that solved it
3. **Break it** with actual usage
4. **Fix it** slightly less ugly
5. **Repeat** until it didn't break anymore

That's it. That's the whole methodology. No sprints, no user stories, no architecture diagrams. Just: "This is broken. Fix it. Ship it. Next."

### What This Actually Proves

**You don't need a plan. You need problems.**

- No CS degree ✓
- No bootcamp ✓
- No roadmap ✓
- No idea what I was building ✓

Just: 3,864 workers who need to be dispatched, and me being too stubborn to say "I can't figure this out."

### What's Next: More Bricks

The migration to `the-board` isn't a "strategic vision." It's: "SQLite is starting to hurt, PostgreSQL might hurt less." Same pattern, bigger scale.

Will I know what I'm building this time? Absolutely not. Will I build it anyway? Obviously.

### For Others Who Don't Know What They're Doing

**Good. Neither did I.**

Here's what actually worked:
- Build the thing in front of you, not the thing you think you should build
- Ship broken code. Users will tell you what matters.
- "Best practices" are just "practices that worked for someone else's problems"
- Your domain expertise > someone else's technical expertise
- One brick at a time. You'll look back and see a building.

The 11 repositories aren't "phases." They're what it looks like when you keep solving problems without knowing where you're going.

Turns out, you don't need to know where you're going. You just need to keep going.

---

**Want to follow more stumbling forward?** The `the-board` repository will document the next 11 repositories I didn't plan.

---

**Last Updated**: October 24, 2024
**Author**: Vincent Keats
**Status**: Living Document - Updated as migration progresses
