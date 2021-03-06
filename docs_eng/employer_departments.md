# Employer's department directory

> Attention! The values in the directories may change at any time. Do not address them directly.

To learn the employer's department list, one should send the `GET` request to
`/employers/{employer_id}/departments`.

This directory is available only for employers.

In case the request is performed successfully, the status `HTTP 200 OK` 
will be returned, and the employer's department list will be returned in
the response body, for example:

```json
{
    "items": [
        {
            "id": "18320489-18320489-dept1",
            "name": "DEPT#1"
        }, {
            "id": "18320489-18320489-dept2",
            "name": "DEPT#2"
        }
    ]
}
```

The `items` element contains the employer's department list.
Each element from `items` has the following fields:

| Name | Type   | Description           |
|------|--------|-----------------------|
| id   | string | Department identifier |
| name | string | Department name       |

In case the current user is not allowed to view the departments of the employer, the code `HTTP 403 Forbidden` will be returned.
