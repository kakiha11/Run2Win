# A/B Testing Guide: Badge System Versions

## Overview

Two distinct versions of the Run2Win app have been created to test different badge system approaches with users.

## Version A: Achievement-Based Badges
**Location:** `version-a/`

### Features:
- **Milestone-focused rewards** for specific accomplishments
- **8 different badge types** ranging from beginner to advanced
- **Visual distinction** between earned (green) and locked (gray) badges
- **Hover effects** on earned badges for engagement

### Badge Categories:
- **First Run** - Complete your first logged run
- **5K Hero** - Run 5 kilometers in a single session
- **Hill Climber** - Gain 500+ feet elevation in one run
- **10K Champion** - Complete a 10 kilometer run
- **Speed Demon** - Run a sub-7 minute mile pace
- **Mountain Goat** - Gain 1000+ feet elevation in one run
- **Century Club** - Log 100 total miles
- **Marathon Ready** - Complete a 26.2 mile run

### User Psychology:
- Appeals to goal-oriented runners
- Encourages pushing personal limits
- Creates long-term objectives

## Version B: Streak-Based Badges
**Location:** `version-b/`

### Features:
- **Consistency-focused rewards** for daily running habits
- **Visual streak counter** with large prominent number
- **Weekly calendar view** showing completed runs
- **Progress bars** toward streak milestones
- **4 streak badge levels** with clear progression

### Badge Categories:
- **Hot Streak** - 7 consecutive days (ACTIVE)
- **Lightning** - 14 consecutive days
- **Superstar** - 30 consecutive days
- **Diamond** - 100 consecutive days

### Visual Elements:
- **Orange/red gradient** for streak counter (urgency/energy)
- **Calendar grid** showing week at a glance
- **Progress indicators** (7/14 days format)
- **Today highlighted** to encourage action

### User Psychology:
- Appeals to habit-building mindset
- Creates daily engagement pressure
- Builds momentum through consistency

## Testing URLs

Start local servers for each version:

```bash
# Version A (Achievement-based)
cd version-a && python3 -m http.server 8001

# Version B (Streak-based)
cd version-b && python3 -m http.server 8002
```

Access at:
- Version A: `http://localhost:8001`
- Version B: `http://localhost:8002`

## Key Differences to Test

| Aspect | Version A | Version B |
|--------|-----------|-----------|
| **Motivation** | Achievement-driven | Consistency-driven |
| **Time Frame** | Long-term goals | Daily habits |
| **Visual Focus** | Badge collection | Streak counter |
| **Engagement** | Milestone celebration | Daily momentum |
| **User Type** | Goal-oriented | Habit-focused |

## Metrics to Track

### Version A (Achievement):
- Badge unlock rates
- Time to first badge
- Long-term engagement
- Distance/elevation improvements

### Version B (Streak):
- Daily return rate
- Streak length distribution
- Streak break recovery
- Consistency over time

## Recommended Test Duration

- **Minimum:** 2 weeks per user
- **Optimal:** 4-6 weeks per user
- **Sample size:** 20-50 users per version

## User Feedback Questions

1. Which badge system motivated you more?
2. Did you check the app daily?
3. Which visual design appealed to you?
4. Did the badges influence your running behavior?
5. Which system would you continue using?
