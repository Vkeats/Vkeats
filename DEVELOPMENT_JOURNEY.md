# The Board: Development Journey

**From Learning to Production** - A chronicle of building a theatre crew dispatch system for IATSE unions

---

## Overview

This document traces the evolution of **The Board** from initial concept to production-ready system, spanning 11 repositories and 16+ months of development (December 2023 - October 2025). What started as a learning project evolved into a comprehensive theatre crew dispatching system processing thousands of SMS messages and managing hundreds of worker assignments.

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

### Phase 2: Early Prototypes (Mar - Jun 2025)

#### **Appv2** (Mar 2025)
**Status**: Archived
**Technologies**: Early web stack exploration
**Purpose**: Second generation application prototype
**Key Developments**:
- Initial exploration of union crew management concepts
- Database modeling experiments
- Early UI/UX patterns

#### **Staff-Manager** (Mar 2025)
**Status**: Archived
**Purpose**: First attempt at crew management system
**Key Features**:
- Basic staff database
- Simple assignment tracking
- Foundation for roster management concepts

#### **Union-Local** (Mar 2025)
**Status**: Archived
**Purpose**: Union-specific workflow exploration
**Key Insights**:
- Understanding IATSE union rules
- Seniority-based assignment concepts
- Worker qualification tracking

---

### Phase 3: Feature Development & Iteration (Mar 2025)

#### **iatse-dispatch** (Mar 2025)
**Status**: Archived
**Purpose**: First dispatch-focused system
**Breakthrough Features**:
- SMS integration concept
- Dispatch workflow design
- Job position management

#### **Algorithm** (Feb - Mar 2025)
*"Union Worker Algorithm App"*

**Status**: Archived
**Purpose**: Intelligent worker assignment algorithms
**Major Innovations**:
- Seniority-based ranking algorithms
- Skill matching logic
- Conflict detection systems
- Availability tracking

**Why It Matters**: This repository established the core business logic that powers automatic worker assignment, a critical feature that survived into the final product.

---

### Phase 4: Integration & Consolidation (Jun - Jul 2025)

#### **UnionManager** (Jun 2025)
**Status**: Archived
**Purpose**: Comprehensive union management platform
**Key Integrations**:
- Combined worker management + dispatch
- Enhanced SMS workflow
- Database schema maturation
- Multi-job support

#### **CallSteward-CSV-Wizard** (Jul 2025)
**Status**: Archived
**Purpose**: Data migration and import tools
**Critical Features**:
- CSV import wizard for CallSteward legacy data
- Skills list parsing
- Worker database import
- Position template system

**Legacy Integration**: This tool enabled migration from CallSteward (existing system) to The Board, a critical requirement for production adoption.

---

### Phase 5: Production Development (Jun - Oct 2025)

#### **crew-caller** (Jun 2025 - Present)
*"does my job for me"* - **CURRENT PRODUCTION SYSTEM**

**Status**: Active Production
**Created**: June 28, 2025
**Last Updated**: October 25, 2025 (Active development)

**Tech Stack**:
- **Frontend**: Next.js 15, React 19, TypeScript, Tailwind CSS + DaisyUI
- **Backend**: 130+ API routes with service layer pattern
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

### Phase 6: Next Generation Architecture (Oct 2025 - Future)

#### **the-board** (Oct 2025 - Future)
*"IATSE 118 Crew Dispatch System - Intelligent one-click dispatch"*

**Status**: In Development (Production Migration Target)
**Created**: October 21, 2025
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
gh repo edit Vkeats/Appv2 --description "Phase 2: Early prototype (Mar 2025)"
gh repo edit Vkeats/Staff-Manager --description "Phase 2: First crew management system (Mar 2025)"
gh repo edit Vkeats/Union-Local --description "Phase 2: Union workflow exploration (Mar 2025)"
gh repo edit Vkeats/iatse-dispatch --description "Phase 3: First dispatch system with SMS (Mar 2025)"
gh repo edit Vkeats/Algorithm --description "Phase 3: Intelligent worker assignment algorithms (Feb-Mar 2025)"
gh repo edit Vkeats/UnionManager --description "Phase 4: Comprehensive integration (Jun 2025)"
gh repo edit Vkeats/CallSteward-CSV-Wizard --description "Phase 4: Legacy data migration tool (Jul 2025)"
gh repo edit Vkeats/crew-caller --description "Phase 5: Production system - IATSE crew dispatch (Jun 2025 - Active)"
gh repo edit Vkeats/the-board --description "Phase 6: Next-gen production system - Cloud-native PostgreSQL (Oct 2025 - In Development)"
```

---

## Migration Plan: crew-caller → the-board

### Overview
The migration from crew-caller to the-board represents a strategic evolution rather than a complete rewrite. The goal is to maintain all core functionality while modernizing infrastructure for better scalability and performance.

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

## Conclusion

This journey from `learning` to `the-board` represents 16+ months of continuous development, iteration, and learning. Each repository played a critical role in building expertise and establishing patterns that ultimately led to a production-ready system managing thousands of crew members and assignments.

**Key Takeaways**:
- **Iteration is valuable**: Each "failed" prototype taught critical lessons
- **Production use drives quality**: Real-world requirements forced robust solutions
- **Documentation pays dividends**: Comprehensive docs enabled rapid refactoring
- **Modern stack matters**: Next.js 15 + TypeScript provided solid foundation
- **Test everything**: Comprehensive testing caught issues before production

The migration to `the-board` represents the natural evolution of this journey, taking proven concepts and scaling them for the next generation of production requirements.

---

**Last Updated**: October 24, 2025
**Author**: Development Team
**Status**: Living Document - Updated as migration progresses
