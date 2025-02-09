#### Jest Options :

`collectCoverage` : Indicates whether the coverage information should be collected while executing the test.

`collectCoverageFrom` : An array of [glob patterns](https://github.com/micromatch/micromatch) indicating a set of files for which coverage information should be collected.

`coverageDirectory` : The directory where Jest should output its coverage files.

`coveragePathIgnorePatterns` : An array of regular expression pattern strings that are matched against all file paths before executing the test.

`coverageReports` : A list of reporter names that Jest uses when writing coverage reports.

```json
{
	...
	"jest": {
		"collectCoverage": true,
		"coverageDirectory": "reports",
		"coveragePathIgnorePatters": ["/node_modules/"],
		"coverageReports": ['html'],
		collecCoverageFrom: ['**/*.{js,jsx}']
	}
	...
}
```

see more about [jest options](https://jestjs.io/docs/configuration#options).

---