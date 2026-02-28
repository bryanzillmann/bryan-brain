# User Permissions Tracker - Project Reference

**GitHub:** https://github.com/bryanzillmann/User-Permission-Tracker (private repo)  
**Stack:** React + Vite + CSS

**Purpose:** Visualize Process Street's user permission matrix — what each of 10 user roles can see/do.

**10 Roles:** Admin, Builder (Edit & View All), Builder (Edit & View own), Builder (View all), Builder (Run), Builder (View), User (Run), User (View), Guest, Anonymous

**8 Permission Categories:** Organization/Personal Settings, Workflows & Runs, My Work & Tasks, Pages, Data Sets, Data Sets - Saved Views, Forms, Acknowledgments
- ~200+ permission actions total
- Permission levels: 0 (❌ no), 1 (✅ yes), 2 (Limited/own), 3 (Special), 4 (Anonymous), 5 (Own & WFRs)

**Built Features:**
1. Sorting — click column headers
2. Search + Highlight — filter by name, highlights in yellow
3. Role Filters — quick toggle buttons
4. Spreadsheet View — sticky left column, color-coded cells
5. Responsive Design

**File Structure:**
```
src/
├── App.jsx
├── PermissionsTable.jsx (main component)
├── PermissionsTable.css
├── data/permissions.js (ROLES, PERMISSION_CATEGORIES, PERMISSION_LABELS)
└── main.jsx
```

**Key Code Patterns:**
- `sortConfig` state tracks sort by category+column
- `getSortedPermissions()` / `getFilteredPermissions()` / `handleSort()`
- Use `originalActionIndex` (.findIndex()) when rendering sorted/filtered data

**GitHub Token:** `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`

**Next Feature Ideas:** Export CSV/PDF, role comparison, inverted view, role summary stats, dark mode

---

## Coding Rules (Learned from this project)
- Edit → test locally → push → tell Tony to pull. Never skip steps.
- Always use feature branches + PRs. Never push to main.
- Verify icon/library names before using. Test, don't guess.
- Tony is not technical — I solve problems, I don't ask him for technical answers.
- Always give Tony exact terminal commands after pushing.
- Git workflow: `git checkout -b feature/name` → edit → `git add . && git commit -m "..."` → `git push origin feature/name` → Tony creates PR.
