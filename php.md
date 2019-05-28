# use statement for anonymus function

for example like that:
```php
        $trans = $this->get('translator');
        $industries = $data['profile']['dynaJobsJobSectors'];
        $data['profile']['dynaJobsJobSectors'] = array_map(
            function ($industry) use ($trans) {
                return $trans->trans('je_jobExperienceDynaJobsSector.'.$industry, array(), 'sourcer');
            },
            $industries
        );

```
