Option 1: Deploy shift all traffic at once
Option 2: I want to manage the migration from v1 to v2
	Step 1: Deploy v2 without shifting traffic
		`gcloud app deploy --no-promote`
	Step 2: Shift traffic to v2:
		Option 1: Migrate all at once to v2
			```gcloud app services set-traffic s1 --splits v2=1```
		Option 2(Gradual Migration): Gradually shift traffic to c2. Add `--migrate` option
		Option 3(Splitting): Control the pace of migration
			`gcloud app services set-traffic s1 --splits=v2.5,v1=.5`
			Useful to perform A/B testing