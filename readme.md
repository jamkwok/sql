# SQL

## Selecting multiple tables and renaming columns if duplicates

## Example 1
```
select su.email,h.NAME hotelier_name, h.address_line_1 , h.address_line_2, h.address_suburb, h.address_state, h.address_post_code, p.name partner_name, p.code partner_code, w.name whitelist_name ,w.code whitelist_code from system_user as su, `system_user_hotelier` as suh, hotelier as h, partner as p, white_label as w
where su.id = suh.id and suh.`HOTELIER_ID` = h.`HOTELIER_ID` and su.partner_id = p.id and su.white_label_id = w.id
order by su.email
```
