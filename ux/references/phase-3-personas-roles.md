# Phase 3: Personas and roles

**Goal:** Turn the research into a small set of personas the team designs for, and a
precise definition of what each role can see and do.

**Done when:** Every user group maps to a persona, every persona maps to one or more
roles, and the permissions matrix has no "TBD" cells.

## Personas

Create one persona per meaningfully different group, usually 3 to 5. Two groups
belong in the same persona only if their goals, context and permissions match.

Base every persona on phase 2 findings. Never invent traits that weren't discussed;
if something is needed but unknown, mark it as an assumption.

Persona fields:
- ID, name and role (for example, P1 Priya, purchase manager)
- One-line summary
- Goals (top 3)
- Frustrations (top 3)
- Context: devices, environment, frequency, tech comfort
- What they need most from this product
- Quote that captures their attitude (only if based on something said in research)
- Evidence level

Mark one persona as **primary**: when trade-offs come up, the primary persona wins
unless a decision says otherwise.

## Roles and permissions

Personas describe people; roles describe system access. One persona can hold several
roles, and several personas can share a role.

Question areas:
- List every role, including admin, support and read-only roles.
- For each main object (orders, invoices, users and so on), which roles can view,
  create, edit, delete, approve, export?
- Data scope: what slice of data each role sees (own records, own team, own company,
  everything). This is critical for customer-facing portals.
- Can one user hold multiple roles? How do they switch?
- Account lifecycle: who creates accounts, invites, deactivates? Self sign-up or
  invite only? What happens to a deactivated user's records?
- Hierarchy: parent and child companies, branches, teams.
- Sensitive fields that some roles must not see (prices, margins, personal data).
- Impersonation or "view as" for support staff?

## Traps to probe

- "Admin can do everything": ask whether admins should really delete financial
  records, and whether actions need an audit trail.
- Customer portals: confirm a user can never see another company's data, and how
  multi-site customers work.
- Roles copied from the org chart rather than from what people do in the system.

## Spec section 3 structure

3.1 Personas (cards) · 3.2 Primary persona · 3.3 Roles list · 3.4 Permissions matrix
(object × action × role) · 3.5 Data scope rules · 3.6 Account lifecycle
