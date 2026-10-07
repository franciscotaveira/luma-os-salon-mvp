# Review Checklist: LUMA OS SALON MVP

## Functional review
- [ ] appointment creation works
- [ ] appointment conflicts are prevented
- [ ] scheduling grid renders correctly
- [ ] status updates work
- [ ] client history is updated
- [ ] commission logic is calculated and logged
- [ ] dashboard metrics are visible and accurate

## Security review
- [ ] no secrets in source
- [ ] environment variables documented
- [ ] auth works
- [ ] roles enforced
- [ ] sensitive data protected
- [ ] RLS reviewed
- [ ] logs for critical actions exist

## Architecture review
- [ ] modules are isolated
- [ ] business logic not mixed into UI
- [ ] API/actions are clear
- [ ] event/webhook layer exists
- [ ] future integrations are prepared without coupling

## DevOps review
- [ ] Docker local environment runs
- [ ] env example is complete
- [ ] health checks exist
- [ ] production deploy config reviewed
- [ ] backups defined
- [ ] monitoring thresholds considered

## Financial review
- [ ] commissions are auditable
- [ ] values are stored with logs
- [ ] calculation is deterministic
- [ ] payout data is traceable

## QA review
- [ ] all acceptance criteria tested
- [ ] regression scenarios reviewed
- [ ] edge cases considered
- [ ] bug reports reviewed

## Definition of done
A task or change is done only if:
- [ ] feature works
- [ ] tests pass
- [ ] docs updated
- [ ] security reviewed
- [ ] acceptance criteria validated
- [ ] diff reviewed
- [ ] deployment impact assessed
