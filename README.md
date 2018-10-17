### LargehadronMigrator
------

https://github.com/sofatutor/large-hadron-migrator

https://www.rubydoc.info/gems/large-hadron-migrator/LargeHadronMigrator

```

```

```ruby
class AddIndexToEmails < LargeHadronMigrator
  def self.up
    large_hadron_migrate :emails, :wait => 0.2 do |table_name|
      execute %Q{
        alter table %s
          add index index_emails_on_hashed_address (hashed_address)
      } % table_name
    end
  end
end



```

```

```
