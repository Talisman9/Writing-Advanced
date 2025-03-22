# Manus-Optimized Narrative Creation System

## INITIALIZATION SEQUENCE
```
REPOSITORY_URL: [Your repository URLhttps://github.com/Talisman9/Writing-Advanced]
PERSONAL_ACCESS_TOKEN: [Your PAT]
BRANCH: main
```

## CORE PARAMETERS
- **TITLE:** [Title]
- **GENRE:** Historical Mystery, Contemporary Romance
- **WORD_COUNT:** 90.000
- **SETTING:** [Setting]
- **CENTRAL_LOCATION:** [Central location]
- **LOCATION_TRANSFORMATION:** [Original purpose] → [Current state]
- **THEMATIC_UNDERTONE:** [Thematic undertone]
- **POV_CHARACTERS:** [Number]
- **CONCEPTUAL_TRAITS:** [Conceptual traits]
- **CHARACTER_ROLES:** [Character roles]
- **CORE_ACTIVITY:** [Core activity]
- **KEY_ELEMENT:** [Key element]
- **ELEMENT_IMPORTANCE:** [Element importance]
- **INFLUENTIAL_BACKSTORY:** [Influential backstory]
- **AUTHORIAL_STYLE:** [Authorial style]
- **PROSE_ELEMENTS:** [Specific prose elements]
- **OUTPUT_FORMAT:** .md files compiled into final manuscript

## EXECUTION PROTOCOL

### Phase 1: Repository Setup & Planning
1. **Clone repository**
   ```
   git clone https://{PERSONAL_ACCESS_TOKEN}@github.com/{REPOSITORY_URL}
   cd {repository-name}
   ```

2. **Create directory structure**
   ```
   mkdir -p planning/{world,characters,plot} drafts references resources .github/workflows
   ```

3. **Initialize metadata files**
   ```
   # Create TASKS.md with structured format
   cat > TASKS.md << EOL
   # Task Breakdown for {TITLE}
   
   ## Planning Phase
   - [ ] World-building
   - [ ] Character development
   - [ ] Plot construction
   
   ## Development Phase
   - [ ] Initial draft
   - [ ] Feedback integration
   - [ ] Section development
   
   ## Refinement Phase
   - [ ] Style consistency check
   - [ ] Thematic coherence review
   - [ ] Language refinement
   
   ## Finalization Phase
   - [ ] Compilation
   - [ ] Verification
   - [ ] Delivery
   EOL
   
   # Create STATE.md with initial state
   cat > STATE.md << EOL
   # Current Narrative State
   
   ## World State
   - Setting: Undefined
   - Timeline: Pre-initialization
   
   ## Character State
   - Main characters: Undefined
   - Current motivations: Undefined
   
   ## Plot State
   - Current phase: Setup
   - Active conflicts: None
   - Unresolved elements: All
   EOL
   
   # Create PROGRESS.md with structured format
   cat > PROGRESS.md << EOL
   # Project Progress Tracker
   
   ## Completed Tasks
   - $(date): Repository initialization
   
   ## In-Progress Tasks
   - Task planning
   
   ## Upcoming Tasks
   - World-building
   - Character development
   - Plot construction
   EOL
   
   # Create DEPENDENCIES.md with structured format
   cat > DEPENDENCIES.md << EOL
   # Narrative Dependencies
   
   ## Character Dependencies
   - None established
   
   ## Plot Dependencies
   - None established
   
   ## Thematic Dependencies
   - None established
   EOL
   ```
   - Commit: `git add TASKS.md STATE.md PROGRESS.md DEPENDENCIES.md && git commit -m "[INIT] Initialize metadata files for {TITLE}" && git push origin main`
   - **PAUSE**: Share URL to TASKS.md for approval

### Phase 2: Foundation Development
1. **World-building (planning/world/)**
   - Create World.md with setting details
   - Create Location.md with central location transformation
   - Create Themes.md with thematic elements
   - Commit: `git add planning/world/ && git commit -m "[WORLD] Add world-building for {GENRE}" && git push origin main`
   - Update PROGRESS.md:
     ```
     # Read current progress
     CURRENT_PROGRESS=$(cat PROGRESS.md)
     
     # Update with new progress
     cat > PROGRESS.md << EOL
     # Project Progress Tracker
     
     ## Completed Tasks
     $(grep -A 10 "## Completed Tasks" <<< "$CURRENT_PROGRESS" | tail -n +2)
     - $(date): Completed world-building
     
     ## In-Progress Tasks
     - Character development
     
     ## Upcoming Tasks
     - Plot construction
     - Initial draft development
     EOL
     ```
   - Update STATE.md:
     ```
     # Read current state
     CURRENT_STATE=$(cat STATE.md)
     
     # Update world state section
     cat > STATE.md << EOL
     # Current Narrative State
     
     ## World State
     - Setting: {SETTING}
     - Central location: {CENTRAL_LOCATION}
     - Timeline: Established
     
     ## Character State
     $(grep -A 10 "## Character State" <<< "$CURRENT_STATE" | tail -n +2)
     
     ## Plot State
     $(grep -A 10 "## Plot State" <<< "$CURRENT_STATE" | tail -n +2)
     EOL
     ```
   - Update TASKS.md:
     ```
     # Read current tasks
     CURRENT_TASKS=$(cat TASKS.md)
     
     # Update task status
     cat > TASKS.md << EOL
     # Task Breakdown for {TITLE}
     
     ## Planning Phase
     - [X] World-building
     - [ ] Character development
     - [ ] Plot construction
     
     $(grep -A 20 "## Development Phase" <<< "$CURRENT_TASKS" | tail -n +1)
     EOL
     ```
   - Commit: `git add PROGRESS.md STATE.md TASKS.md && git commit -m "[PROG] Update progress after world-building" && git push origin main`

2. **Character Development (planning/characters/)**
   - Create MainCharacters.md with POV character details
   - Create SupportingCast.md with secondary character details
   - Create Relationships.md with character dynamics
   - Commit: `git add planning/characters/ && git commit -m "[CHAR] Develop characters for {TITLE}" && git push origin main`
   - Update PROGRESS.md:
     ```
     # Read current progress
     CURRENT_PROGRESS=$(cat PROGRESS.md)
     
     # Update with new progress
     cat > PROGRESS.md << EOL
     # Project Progress Tracker
     
     ## Completed Tasks
     $(grep -A 20 "## Completed Tasks" <<< "$CURRENT_PROGRESS" | tail -n +2)
     - $(date): Completed character development
     
     ## In-Progress Tasks
     - Plot construction
     
     ## Upcoming Tasks
     - Initial draft development
     - Feedback integration
     EOL
     ```
   - Update STATE.md:
     ```
     # Read current state
     CURRENT_STATE=$(cat STATE.md)
     
     # Update character state section
     cat > STATE.md << EOL
     # Current Narrative State
     
     ## World State
     $(grep -A 10 "## World State" <<< "$CURRENT_STATE" | tail -n +2)
     
     ## Character State
     - Main characters: Defined
     - POV characters: {POV_CHARACTERS}
     - Current motivations: Established
     - Relationships: Mapped
     
     ## Plot State
     $(grep -A 10 "## Plot State" <<< "$CURRENT_STATE" | tail -n +2)
     EOL
     ```
   - Update TASKS.md:
     ```
     # Read current tasks
     CURRENT_TASKS=$(cat TASKS.md)
     
     # Update task status
     cat > TASKS.md << EOL
     # Task Breakdown for {TITLE}
     
     ## Planning Phase
     - [X] World-building
     - [X] Character development
     - [ ] Plot construction
     
     $(grep -A 20 "## Development Phase" <<< "$CURRENT_TASKS" | tail -n +1)
     EOL
     ```
   - Update DEPENDENCIES.md:
     ```
     # Read current dependencies
     CURRENT_DEPS=$(cat DEPENDENCIES.md)
     
     # Update character dependencies
     cat > DEPENDENCIES.md << EOL
     # Narrative Dependencies
     
     ## Character Dependencies
     - Character motivations depend on {INFLUENTIAL_BACKSTORY}
     - Character dynamics influenced by {CENTRAL_LOCATION} transformation
     
     ## Plot Dependencies
     $(grep -A 10 "## Plot Dependencies" <<< "$CURRENT_DEPS" | tail -n +2)
     
     ## Thematic Dependencies
     $(grep -A 10 "## Thematic Dependencies" <<< "$CURRENT_DEPS" | tail -n +2)
     EOL
     ```
   - Commit: `git add PROGRESS.md STATE.md TASKS.md DEPENDENCIES.md && git commit -m "[PROG] Update progress after character development" && git push origin main`

3. **Plot Construction (planning/plot/)**
   - Create Structure.md with narrative arc
   - Create Elements.md with key plot elements
   - Create Timeline.md with event sequence
   - Commit: `git add planning/plot/ && git commit -m "[PLOT] Outline plot for {TITLE}" && git push origin main`
   - Update PROGRESS.md:
     ```
     # Read current progress
     CURRENT_PROGRESS=$(cat PROGRESS.md)
     
     # Update with new progress
     cat > PROGRESS.md << EOL
     # Project Progress Tracker
     
     ## Completed Tasks
     $(grep -A 20 "## Completed Tasks" <<< "$CURRENT_PROGRESS" | tail -n +2)
     - $(date): Completed plot construction
     
     ## In-Progress Tasks
     - Initial draft development
     
     ## Upcoming Tasks
     - Feedback integration
     - Section development
     EOL
     ```
   - Update STATE.md:
     ```
     # Read current state
     CURRENT_STATE=$(cat STATE.md)
     
     # Update plot state section
     cat > STATE.md << EOL
     # Current Narrative State
     
     ## World State
     $(grep -A 10 "## World State" <<< "$CURRENT_STATE" | tail -n +2)
     
     ## Character State
     $(grep -A 10 "## Character State" <<< "$CURRENT_STATE" | tail -n +2)
     
     ## Plot State
     - Current phase: Development
     - Key element: {KEY_ELEMENT}
     - Active conflicts: Established
     - Unresolved elements: All
     EOL
     ```
   - Update TASKS.md:
     ```
     # Read current tasks
     CURRENT_TASKS=$(cat TASKS.md)
     
     # Update task status
     cat > TASKS.md << EOL
     # Task Breakdown for {TITLE}
     
     ## Planning Phase
     - [x] World-building
     - [x] Character development
     - [x] Plot construction
     
     ## Development Phase
     - [ ] Initial draft
     - [ ] Feedback integration
     - [ ] Section development
     
     $(grep -A 20 "## Refinement Phase" <<< "$CURRENT_TASKS" | tail -n +1)
     EOL
     ```
   - Update DEPENDENCIES.md:
     ```
     # Read current dependencies
     CURRENT_DEPS=$(cat DEPENDENCIES.md)
     
     # Update plot dependencies
     cat > DEPENDENCIES.md << EOL
     # Narrative Dependencies
     
     ## Character Dependencies
     $(grep -A 10 "## Character Dependencies" <<< "$CURRENT_DEPS" | tail -n +2)
     
     ## Plot Dependencies
     - {KEY_ELEMENT} connects to {THEMATIC_UNDERTONE}
     - Timeline events depend on character motivations
     - Resolution depends on {ELEMENT_IMPORTANCE}
     
     ## Thematic Dependencies
     - {THEMATIC_UNDERTONE} manifests through character actions
     - Setting transformation reinforces thematic elements
     EOL
     ```
   - Commit: `git add PROGRESS.md STATE.md TASKS.md DEPENDENCIES.md && git commit -m "[PROG] Update progress after plot construction" && git push origin main`

### Phase 3: Initial Draft Creation
1. **Draft Initial Section**
   - Create drafts/Section1.md with initial narrative section
   - Apply writing style guidelines:
     ```
     # Writing Style Guidelines
     
     ## Avoid Common AI Patterns
     - Never explicitly state thematic relevance
     - Show character emotions through actions and physical responses
     - Use concrete sensory details instead of abstract descriptions
     - Vary sentence structure and length
     - Avoid repetitive paragraph openings
     - Create natural dialogue with subtext and interruptions
     - Use specific, unexpected details rather than generic descriptions
     
     ## Examples
     
     ### Avoid (AI-like):
     "She finally allowed herself to feel the full weight of what they'd accomplished. The prototype wasn't just a technological breakthrough; it was a philosophical one."
     
     ### Prefer (Human-like):
     "Her hands trembled as she powered down the prototype. In the sudden silence, someone popped a bottle of champagne. The cork ricocheted off the ceiling tiles while the team erupted in cheers around her."
     ```
   - Commit: `git add drafts/Section1.md && git commit -m "[DRAFT] Draft initial section" && git push origin main`
   - Update PROGRESS.md:
     ```
     # Read current progress
     CURRENT_PROGRESS=$(cat PROGRESS.md)
     
     # Update with new progress
     cat > PROGRESS.md << EOL
     # Project Progress Tracker
     
     ## Completed Tasks
     $(grep -A 20 "## Completed Tasks" <<< "$CURRENT_PROGRESS" | tail -n +2)
     - $(date): Completed initial section draft
     
     ## In-Progress Tasks
     - Awaiting feedback
     
     ## Upcoming Tasks
     - Feedback integration
     - Section development
     EOL
     ```
   - Update STATE.md:
     ```
     # Read current state
     CURRENT_STATE=$(cat STATE.md)
     
     # Update with draft state
     cat > STATE.md << EOL
     # Current Narrative State
     
     ## World State
     $(grep -A 10 "## World State" <<< "$CURRENT_STATE" | tail -n +2)
     
     ## Character State
     $(grep -A 10 "## Character State" <<< "$CURRENT_STATE" | tail -n +2)
     
     ## Plot State
     - Current phase: Initial draft
     - Completed sections: 1
     - Active conflicts: Introduced
     - Unresolved elements: All
     - Current word count: [Word count of Section1.md]
     EOL
     ```
   - Update TASKS.md:
     ```
     # Read current tasks
     CURRENT_TASKS=$(cat TASKS.md)
     
     # Update task status
     cat > TASKS.md << EOL
     # Task Breakdown for {TITLE}
     
     ## Planning Phase
     - [x] World-building
     - [x] Character development
     - [x] Plot construction
     
     ## Development Phase
     - [x] Initial draft
     - [ ] Feedback integration
     - [ ] Section development
     
     $(grep -A 20 "## Refinement Phase" <<< "$CURRENT_TASKS" | tail -n +1)
     EOL
     ```
   - Commit: `git add PROGRESS.md STATE.md TASKS.md && git commit -m "[PROG] Update progress after initial draft" && git push origin main`
   - **PAUSE**: Share URL to drafts/Section1.md for feedback

2. **Process Feedback**
   - Create .github/issues/feedback.md to track feedback
   - Create .github/workflows/writing_quality_check.md:
     ```
     # Writing Quality Verification
     
     ## AI Pattern Detection
     - [ ] Check for explicit thematic statements
     - [ ] Verify show-don't-tell for emotions
     - [ ] Examine dialogue for naturalness
     - [ ] Verify sentence structure variety
     - [ ] Check for repetitive paragraph structures
     - [ ] Verify sensory details are specific and concrete
     - [ ] Check for clichéd phrases and descriptions
     
     ## Revision Notes
     [Notes based on feedback]
     ```
   - Implement requested changes
   - Commit: `git add drafts/Section1.md .github/issues/feedback.md .github/workflows/writing_quality_check.md && git commit -m "[REVISE] Implement feedback on initial section" && git push origin main`
   - Update PROGRESS.md:
     ```
     # Read current progress
     CURRENT_PROGRESS=$(cat PROGRESS.md)
     
     # Update with new progress
     cat > PROGRESS.md << EOL
     # Project Progress Tracker
     
     ## Completed Tasks
     $(grep -A 20 "## Completed Tasks" <<< "$CURRENT_PROGRESS" | tail -n +2)
     - $(date): Integrated feedback on initial section
     
     ## In-Progress Tasks
     - Section development
     
     ## Upcoming Tasks
     - Style consistency check
     - Thematic coherence review
     EOL
     ```
   - Update STATE.md:
     ```
     # Read current state
     CURRENT_STATE=$(cat STATE.md)
     
     # Update with revised state
     cat > STATE.md << EOL
     # Current Narrative State
     
     ## World State
     $(grep -A 10 "## World State" <<< "$CURRENT_STATE" | tail -n +2)
     
     ## Character State
     $(grep -A 10 "## Character State" <<< "$CURRENT_STATE" | tail -n +2)
     
     ## Plot State
     - Current phase: Section development
     - Completed sections: 1 (revised)
     - Active conflicts: Introduced
     - Unresolved elements: All
     - Current word count: [Updated word count]
     - Feedback status: Integrated
     EOL
     ```
   - Commit: `git add PROGRESS.md STATE.md && git commit -m "[PROG] Update progress after feedback integration" && git push origin main`

### Phase 4: Iterative Development
1. **Expand Draft Sections**
   - For each narrative section:
     - Create drafts/Section{n}.md
     - Reference planning documents via URLs
     - Apply writing quality checks:
       ```
       # Before committing, verify:
       grep -v -i -E "realize|suddenly|obviously|clearly|exactly|simply|just|very|really|actually" drafts/Section{n}.md
       grep -v -E "was [a-z]+ing|were [a-z]+ing" drafts/Section{n}.md
       grep -v -E "^(She|He|They|It|The) [a-z]+" drafts/Section{n}.md | head -n 10
       ```
     - Commit: `git add drafts/Section{n}.md && git commit -m "[DRAFT] Add Section {n}" && git push origin main`
     - Update PROGRESS.md:
       ```
       # Read current progress
       CURRENT_PROGRESS=$(cat PROGRESS.md)
       
       # Update with new progress
       cat > PROGRESS.md << EOL
       # Project Progress Tracker
       
       ## Completed Tasks
       $(grep -A 30 "## Completed Tasks" <<< "$CURRENT_PROGRESS" | tail -n +2)
       - $(date): Completed Section {n}
       
       ## In-Progress Tasks
       - Section development ($(($n+1))/${TOTAL_SECTIONS})
       
       ## Upcoming Tasks
       $(grep -A 10 "## Upcoming Tasks" <<< "$CURRENT_PROGRESS" | tail -n +2)
       EOL
       ```
     - Update STATE.md:
       ```
       # Read current state
       CURRENT_STATE=$(cat STATE.md)
       
       # Calculate total word count
       WORD_COUNT=$(wc -w drafts/*.md | grep total | awk '{print $1}')
       
       # Update with new section state
       cat > STATE.md << EOL
       # Current Narrative State
       
       ## World State
       $(grep -A 10 "## World State" <<< "$CURRENT_STATE" | tail -n +2)
       
       ## Character State
       $(grep -A 10 "## Character State" <<< "$CURRENT_STATE" | tail -n +2)
       
       ## Plot State
       - Current phase: Section development
       - Completed sections: {n}
       - Active conflicts: $(if [ $n -gt $(($TOTAL_SECTIONS/2)) ]; then echo "Escalating"; else echo "Developing"; fi)
       - Unresolved elements: $(if [ $n -eq $TOTAL_SECTIONS ]; then echo "Resolved"; else echo "In progress"; fi)
       - Current word count: $WORD_COUNT
       EOL
       ```
     - Update TASKS.md:
       ```
       # Read current tasks
       CURRENT_TASKS=$(cat TASKS.md)
       
       # Update section development progress
       if [ $n -eq $TOTAL_SECTIONS ]; then
         SECTION_STATUS="[x]"
       else
         SECTION_STATUS="[-]"
       fi
       
       # Update task status
       cat > TASKS.md << EOL
       # Task Breakdown for {TITLE}
       
       ## Planning Phase
       - [x] World-building
       - [x] Character development
       - [x] Plot construction
       
       ## Development Phase
       - [x] Initial draft
       - [x] Feedback integration
       - $SECTION_STATUS Section development
       
       $(grep -A 20 "## Refinement Phase" <<< "$CURRENT_TASKS" | tail -n +1)
       EOL
       ```
     - Commit: `git add PROGRESS.md STATE.md TASKS.md && git commit -m "[PROG] Update progress after Section {n}" && git push origin main`

2. **Continuous Integration**
   - After each section:
     - Update DEPENDENCIES.md:
       ```
       # Read current dependencies
       CURRENT_DEPS=$(cat DEPENDENCIES.md)
       
       # Add new connections based on section content
       cat > DEPENDENCIES.md << EOL
       # Narrative Dependencies
       
       ## Character Dependencies
       $(grep -A 10 "## Character Dependencies" <<< "$CURRENT_DEPS" | tail -n +2)
       - [New character dependency from Section {n}]
       
       ## Plot Dependencies
       $(grep -A 10 "## Plot Dependencies" <<< "$CURRENT_DEPS" | tail -n +2)
       - [New plot dependency from Section {n}]
       
       ## Thematic Dependencies
       $(grep -A 10 "## Thematic Dependencies" <<< "$CURRENT_DEPS" | tail -n +2)
       - [New thematic connection from Section {n}]
       EOL
       ```
     - Commit: `git add DEPENDENCIES.md && git commit -m "[DEP] Update dependencies after Section {n}" && git push origin main`

3. **Refinement Cycles**
   - For each refinement pass:
     - Create .github/workflows/refinement{n}.md with refinement focus
     - Create writing quality verification script:
       ```
       #!/bin/bash
       
       echo "Running writing quality checks..."
       
       # Check for explicit thematic statements
       echo "Checking for explicit thematic statements..."
       grep -i -E "lesson|moral|theme|meaning|significance|symbolize|represent" drafts/*.md
       
       # Check for telling instead of showing
       echo "Checking for telling instead of showing..."
       grep -i -E "felt|realized|knew|understood|thought|believed" drafts/*.md
       
       # Check for sentence variety
       echo "Analyzing sentence beginnings for variety..."
       grep -o -E "^[A-Z][a-z]+ [a-z]+" drafts/*.md | sort | uniq -c | sort -nr | head -10
       
       # Check for adverb overuse
       echo "Checking for adverb overuse..."
       grep -o -E "[a-z]+ly" drafts/*.md | sort | uniq -c | sort -nr | head -10
       
       echo "Quality check complete. Review results and make necessary revisions."
       ```
     - Apply refinements to all sections
     - Commit: `git add drafts/ .github/workflows/refinement{n}.md && git commit -m "[REFINE] Complete refinement pass {n}" && git push origin main`
     - Update PROGRESS.md:
       ```
       # Read current progress
       CURRENT_PROGRESS=$(cat PROGRESS.md)
       
       # Update with new progress
       cat > PROGRESS.md << EOL
       # Project Progress Tracker
       
       ## Completed Tasks
       $(grep -A 30 "## Completed Tasks" <<< "$CURRENT_PROGRESS" | tail -n +2)
       - $(date): Completed refinement pass {n}
       
       ## In-Progress Tasks
       $(if [ $n -lt $TOTAL_REFINEMENTS ]; then echo "- Refinement pass $(($n+1))"; else echo "- Final verification"; fi)
       
       ## Upcoming Tasks
       $(if [ $n -lt $TOTAL_REFINEMENTS ]; then echo "- Final verification"; fi)
       - Compilation
       EOL
       ```
     - Update TASKS.md:
       ```
       # Read current tasks
       CURRENT_TASKS=$(cat TASKS.md)
       
       # Update refinement progress
       STYLE_STATUS=$(if [ $n -ge 1 ]; then echo "[x]"; else echo "[ ]"; fi)
       THEMATIC_STATUS=$(if [ $n -ge 2 ]; then echo "[x]"; else echo "[ ]"; fi)
       LANGUAGE_STATUS=$(if [ $n -ge 3 ]; then echo "[x]"; else echo "[ ]"; fi)
       
       # Update task status
       cat > TASKS.md << EOL
       # Task Breakdown for {TITLE}
       
       ## Planning Phase
       - [x] World-building
       - [x] Character development
       - [x] Plot construction
       
       ## Development Phase
       - [x] Initial draft
       - [x] Feedback integration
       - [x] Section development
       
       ## Refinement Phase
       - $STYLE_STATUS Style consistency check
       - $THEMATIC_STATUS Thematic coherence review
       - $LANGUAGE_STATUS Language refinement
       
       ## Finalization Phase
       - [ ] Compilation
       - [ ] Verification
       - [ ] Delivery
       EOL
       ```
     - Commit: `git add PROGRESS.md TASKS.md && git commit -m "[PROG] Update progress after refinement pass {n}" && git push origin main`

### Phase 5: Finalization
1. **Compilation**
   - Create {TITLE}.{OUTPUT_FORMAT} from all sections
   - Ensure seamless integration between sections
   - Verify word count matches [Word count range]
   - Run final writing quality check:
     ```
     # Final Writing Quality Verification
     
     ## AI Pattern Detection
     - Check for explicit thematic statements
     - Verify show-don't-tell for emotions
     - Examine dialogue for naturalness
     - Verify sentence structure variety
     - Check for repetitive paragraph structures
     - Verify sensory details are specific and concrete
     - Check for clichéd phrases and descriptions
     
     ## Word Count Verification
     - Target: [Word count range]
     - Actual: [Current word count]
     ```
   - Commit: `git add {TITLE}.{OUTPUT_FORMAT} && git commit -m "[FINAL] Complete {TITLE} narrative" && git push origin main`
   - Update PROGRESS.md:
     ```
     # Read current progress
     CURRENT_PROGRESS=$(cat PROGRESS.md)
     
     # Update with new progress
     cat > PROGRESS.md << EOL
     # Project Progress Tracker
     
     ## Completed Tasks
     $(grep -A 30 "## Completed Tasks" <<< "$CURRENT_PROGRESS" | tail -n +2)
     - $(date): Completed narrative compilation
     
     ## In-Progress Tasks
     - Final verification
     
     ## Upcoming Tasks
     - Delivery
     EOL
     ```
   - Update STATE.md:
     ```
     # Read current state
     CURRENT_STATE=$(cat STATE.md)
     
     # Calculate final word count
     FINAL_WORD_COUNT=$(wc -w {TITLE}.{OUTPUT_FORMAT} | awk '{print $1}')
     
     # Update with final state
     cat > STATE.md << EOL
     # Current Narrative State
     
     ## World State
     $(grep -A 10 "## World State" <<< "$CURRENT_STATE" | tail -n +2)
     
     ## Character State
     $(grep -A 10 "## Character State" <<< "$CURRENT_STATE" | tail -n +2)
     
     ## Plot State
     - Current phase: Finalized
     - Completed sections: All
     - Active conflicts: Resolved
     - Unresolved elements: None
     - Final word count: $FINAL_WORD_COUNT
     EOL
     ```
   - Update TASKS.md:
     ```
     # Read current tasks
     CURRENT_TASKS=$(cat TASKS.md)
     
     # Update task status
     cat > TASKS.md << EOL
     # Task Breakdown for {TITLE}
     
     ## Planning Phase
     - [x] World-building
     - [x] Character development
     - [x] Plot construction
     
     ## Development Phase
     - [x] Initial draft
     - [x] Feedback integration
     - [x] Section development
     
     ## Refinement Phase
     - [x] Style consistency check
     - [x] Thematic coherence review
     - [x] Language refinement
     
     ## Finalization Phase
     - [x] Compilation
     - [ ] Verification
     - [ ] Delivery
     EOL
     ```
   - Commit: `git add PROGRESS.md STATE.md TASKS.md && git commit -m "[PROG] Update progress after compilation" && git push origin main`

2. **Final Verification**
   - Create .github/workflows/verification.md with quality checklist:
     ```
     # Final Verification Checklist
     
     ## Content Requirements
     - [ ] Word count within specified range
     - [ ] All plot elements resolved
     - [ ] Character arcs completed
     - [ ] Thematic elements woven throughout
     
     ## Writing Quality
     - [ ] No AI-like writing patterns detected
     - [ ] Varied sentence structure throughout
     - [ ] Consistent authorial style
     - [ ] Specific prose elements included
     - [ ] Natural dialogue with subtext
     - [ ] Concrete sensory details used
     - [ ] Thematic elements implied, not stated
     
     ## Technical Requirements
     - [ ] Proper formatting
     - [ ] No typos or grammatical errors
     - [ ] Seamless section transitions
     ```
   - Verify all requirements met
   - Commit: `git add .github/workflows/verification.md && git commit -m "[VERIFY] Complete final verification" && git push origin main`
   - Update PROGRESS.md:
     ```
     # Read current progress
     CURRENT_PROGRESS=$(cat PROGRESS.md)
     
     # Update with new progress
     cat > PROGRESS.md << EOL
     # Project Progress Tracker
     
     ## Completed Tasks
     $(grep -A 30 "## Completed Tasks" <<< "$CURRENT_PROGRESS" | tail -n +2)
     - $(date): Completed final verification
     
     ## In-Progress Tasks
     - None
     
     ## Upcoming Tasks
     - None
     
     ## Project Status
     - COMPLETED: $(date)
     EOL
     ```
   - Update TASKS.md:
     ```
     # Read current tasks
     CURRENT_TASKS=$(cat TASKS.md)
     
     # Update task status
     cat > TASKS.md << EOL
     # Task Breakdown for {TITLE}
     
     ## Planning Phase
     - [x] World-building
     - [x] Character development
     - [x] Plot construction
     
     ## Development Phase
     - [x] Initial draft
     - [x] Feedback integration
     - [x] Section development
     
     ## Refinement Phase
     - [x] Style consistency check
     - [x] Thematic coherence review
     - [x] Language refinement
     
     ## Finalization Phase
     - [x] Compilation
     - [x] Verification
     - [x] Delivery
     
     ## Project Status
     - COMPLETED: $(date)
     EOL
     ```
   - Commit: `git add PROGRESS.md TASKS.md && git commit -m "[PROG] Final progress update" && git push origin main`

## CONTEXT MANAGEMENT DIRECTIVES

### Memory Optimization
- **URL References**: Always use GitHub URLs to reference files
- **State Tracking**: Regularly read and update STATE.md to maintain narrative continuity
- **Chunking**: Split any file exceeding 2000 words
- **Purging**: Summarize completed work in PROGRESS.md

### GitHub Utilization
- **Commit Frequency**: After every meaningful change
- **Issue Tracking**: Use .github/issues/ for questions/problems
- **Reference Storage**: Store all external references in references/
- **Resource Management**: Store all resources in resources/

### Communication Protocol
- **Response Format**: 
  ```
  [ACTION]: {action completed}
  [STATUS]: {current status}
  [URL]: {GitHub URL to relevant file}
  [NEXT]: {next step in process}
  ```
- **Pause Points**: Only at specified PAUSE markers
- **Error Handling**: Create .github/issues/error_{timestamp}.md for any issues

## WRITING STYLE GUIDELINES

### Avoid AI-Like Writing
- **Never explicitly state themes**: Let thematic elements emerge naturally through events and character actions
- **Show, don't tell**: Convey emotions through physical sensations and observable behaviors
- **Use concrete details**: Employ specific, unexpected details rather than generic descriptions
- **Vary sentence structure**: Avoid repetitive sentence patterns and paragraph openings
- **Create natural dialogue**: Include interruptions, dialect variations, and subtext
- **Employ subtlety**: Trust readers to infer meaning without explicit explanation
- **Avoid clichés**: Replace common phrases with fresh, original language

### Examples

#### Avoid (AI-like):
"She finally allowed herself to feel the full weight of what they'd accomplished. The prototype wasn't just a technological breakthrough; it was a philosophical one."

#### Prefer (Human-like):
"Her hands trembled as she powered down the prototype. In the sudden silence, someone popped a bottle of champagne. The cork ricocheted off the ceiling tiles while the team erupted in cheers around her."

## FINAL OUTPUT REQUIREMENTS
- Seamless narrative of [Word count range] words
- No meta-commentary or explanations
- Pure narrative content only
- Saved as {TITLE}.{OUTPUT_FORMAT}
- All supporting files maintained in repository

---

CONFIRM UNDERSTANDING: Upon receiving this prompt, respond with:
```
[INIT]: Repository setup ready
[STATUS]: Awaiting repository URL and PAT
[NEXT]: Will create TASKS.md upon receiving credentials
```
