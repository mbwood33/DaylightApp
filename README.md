# DaylightApp

🧠 Core Features to Implement
1. Daily Log Interface
	- Mood rating (e.g., 1–10 scale with emoji).
	- Customizable symptom checklist from a pre-loaded database (e.g., fatigue, brain fog, palpitations).
	- Medication adherence toggle (pulled from user’s med list).
	- Free-text journal.
2. Medication Tracker
	- Add/search medications (auto-suggest via local or API-based database).
	- Track dose, time, route, PRN or scheduled.
	- Option to log effects or side effects post-dose.
3. Symptom & Med Database
	- Pre-seeded SQL tables for:
	- Common symptoms by category (e.g., psych, neuro, GI).
		- Approved pharmaceuticals (you could use a static JSON import initially).
		- Allow user-defined custom entries.
4. Reminders & Notifications
	- For journal entries, med doses, symptom tracking.
	- Could integrate with browser or email reminders later.
5. Reports & Charts
	- Mood/symptom trends over time.
	- Correlation between medication intake and symptom changes.
	- Export to PDF or CSV.

🗂️ Database Schema Ideas (Simplified)
Table					Key Fields
Users					UserId, Name, Email, PasswordHash
Medications				MedicationId, Name, Dosage, Route, IsCustom
Symptoms				SymptomId, Name, Category, IsCustom
DailyEntries			EntryId, UserId, Date, Mood, JournalText
EntrySymptoms			EntryId, SymptomId
EntryMedications		EntryId, MedicationId, Taken, EffectNotes

Optional: create SymptomTags, MedTags, or ConditionProfiles.

🔧 MudBlazor Components to Use
MudTable with filters for symptom/med search.

MudAutocomplete for medication and symptom entry.

MudRating or MudSlider for mood scale.

MudCharts for trends.

MudDialog for entry forms.

MudTabs to switch views (Log | Meds | Symptoms | Charts).

🚀 Portfolio Appeal
Demonstrates real-world utility (especially for chronic illness/mental health).

Highlights relational DB design and CRUD operations.

Great UX focus if you optimize for neurodivergent users.

Scalable features (e.g., add AI/ML later for trend prediction).