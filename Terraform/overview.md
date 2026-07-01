# String Functions

| Function        | Description                        |
| --------------- | ---------------------------------- |
| `chomp()`       | Remove trailing newline characters |
| `endswith()`    | Check string suffix                |
| `format()`      | Format string                      |
| `formatlist()`  | Format list of strings             |
| `indent()`      | Indent multiline string            |
| `join()`        | Join list into string              |
| `lower()`       | Convert to lowercase               |
| `regex()`       | Match regex                        |
| `regexall()`    | Return all regex matches           |
| `replace()`     | Replace substring                  |
| `split()`       | Split string                       |
| `startswith()`  | Check string prefix                |
| `strcontains()` | Check substring exists             |
| `strrev()`      | Reverse string                     |
| `substr()`      | Extract substring                  |
| `title()`       | Convert to title case              |
| `trim()`        | Remove characters                  |
| `trimprefix()`  | Remove prefix                      |
| `trimspace()`   | Remove whitespace                  |
| `trimsuffix()`  | Remove suffix                      |
| `upper()`       | Convert to uppercase               |

---

# Numeric Functions

| Function     | Description    |
| ------------ | -------------- |
| `abs()`      | Absolute value |
| `ceil()`     | Round up       |
| `floor()`    | Round down     |
| `log()`      | Logarithm      |
| `max()`      | Maximum value  |
| `min()`      | Minimum value  |
| `parseint()` | Parse integer  |
| `pow()`      | Exponentiation |
| `signum()`   | Number sign    |
| `sum()`      | Sum values     |

---

# Collection Functions

| Function            | Description                    |
| ------------------- | ------------------------------ |
| `alltrue()`         | All values true                |
| `anytrue()`         | Any value true                 |
| `chunklist()`       | Split list into chunks         |
| `coalesce()`        | First non-null value           |
| `coalescelist()`    | First non-empty list           |
| `compact()`         | Remove null/empty strings      |
| `concat()`          | Concatenate lists              |
| `contains()`        | Check collection membership    |
| `distinct()`        | Remove duplicates              |
| `element()`         | Retrieve list element          |
| `flatten()`         | Flatten nested lists           |
| `index()`           | Find element index             |
| `keys()`            | Return map keys                |
| `length()`          | Collection size                |
| `lookup()`          | Retrieve map value             |
| `matchkeys()`       | Match keys by values           |
| `merge()`           | Merge maps                     |
| `one()`             | Return single element          |
| `range()`           | Generate integer sequence      |
| `reverse()`         | Reverse list                   |
| `setintersection()` | Common elements                |
| `setproduct()`      | Cartesian product              |
| `setsubtract()`     | Difference of sets             |
| `setunion()`        | Union of sets                  |
| `slice()`           | Extract list segment           |
| `sort()`            | Sort list                      |
| `tolist()`          | Convert to list                |
| `tomap()`           | Convert to map                 |
| `toset()`           | Convert to set                 |
| `transpose()`       | Swap map/list relationships    |
| `values()`          | Return map values              |
| `zipmap()`          | Build map from keys and values |

---

# Encoding Functions

| Function             | Description           |
| -------------------- | --------------------- |
| `base64decode()`     | Decode Base64         |
| `base64encode()`     | Encode Base64         |
| `base64gzip()`       | Compress and encode   |
| `csvdecode()`        | Parse CSV             |
| `jsondecode()`       | Parse JSON            |
| `jsonencode()`       | Generate JSON         |
| `textdecodebase64()` | Decode Base64 text    |
| `textencodebase64()` | Encode text as Base64 |
| `urlencode()`        | URL encode string     |
| `yamldecode()`       | Parse YAML            |
| `yamlencode()`       | Generate YAML         |

---

# Date and Time Functions

| Function          | Description              |
| ----------------- | ------------------------ |
| `formatdate()`    | Format timestamp         |
| `plantimestamp()` | Plan execution timestamp |
| `timeadd()`       | Add duration             |
| `timecmp()`       | Compare timestamps       |
| `timestamp()`     | Current UTC timestamp    |

---

# Filesystem Functions

| Function             | Description            |
| -------------------- | ---------------------- |
| `abspath()`          | Absolute path          |
| `dirname()`          | Directory name         |
| `pathexpand()`       | Expand home directory  |
| `basename()`         | File name              |
| `file()`             | Read text file         |
| `fileexists()`       | Check file exists      |
| `fileset()`          | Match files using glob |
| `filebase64()`       | Read Base64 file       |
| `filebase64sha256()` | SHA256 hash            |
| `filebase64sha512()` | SHA512 hash            |
| `filemd5()`          | MD5 checksum           |
| `filesha1()`         | SHA1 checksum          |
| `filesha256()`       | SHA256 checksum        |
| `filesha512()`       | SHA512 checksum        |
| `templatefile()`     | Render template file   |

---

# Hash and Crypto Functions

| Function       | Description          |
| -------------- | -------------------- |
| `bcrypt()`     | BCrypt password hash |
| `md5()`        | MD5 hash             |
| `sha1()`       | SHA1 hash            |
| `sha256()`     | SHA256 hash          |
| `sha512()`     | SHA512 hash          |
| `rsadecrypt()` | RSA decrypt          |

---

# IP Network Functions

| Function        | Description       |
| --------------- | ----------------- |
| `cidrhost()`    | Host IP from CIDR |
| `cidrnetmask()` | Netmask           |
| `cidrsubnet()`  | Create subnet     |
| `cidrsubnets()` | Multiple subnets  |

---

# Type Conversion Functions

| Function            | Description                     |
| ------------------- | ------------------------------- |
| `can()`             | Test expression validity        |
| `ephemeralasnull()` | Convert ephemeral value to null |
| `issensitive()`     | Check sensitive value           |
| `nonsensitive()`    | Remove sensitivity              |
| `sensitive()`       | Mark value sensitive            |
| `tobool()`          | Convert to boolean              |
| `tonumber()`        | Convert to number               |
| `tostring()`        | Convert to string               |
| `try()`             | First successful expression     |
| `type()`            | Return value type               |

---

# Terraform Block Types

| Block       | Description                  |
| ----------- | ---------------------------- |
| `terraform` | Terraform configuration      |
| `provider`  | Configure provider           |
| `resource`  | Create infrastructure        |
| `data`      | Read existing infrastructure |
| `module`    | Reuse configuration          |
| `variable`  | Input variable               |
| `output`    | Output value                 |
| `locals`    | Local variables              |
| `check`     | Validation checks            |
| `moved`     | Resource migration           |
| `import`    | Import existing resource     |
| `removed`   | Remove resource from state   |

---

# Meta-Arguments

| Meta-Argument | Description                  |
| ------------- | ---------------------------- |
| `count`       | Create multiple resources    |
| `for_each`    | Iterate resources            |
| `depends_on`  | Explicit dependency          |
| `provider`    | Select provider instance     |
| `lifecycle`   | Resource lifecycle rules     |
| `provisioner` | Execute local/remote scripts |
| `connection`  | Connection configuration     |

---

# Lifecycle Arguments

| Argument                | Description              |
| ----------------------- | ------------------------ |
| `create_before_destroy` | Replace safely           |
| `prevent_destroy`       | Block deletion           |
| `ignore_changes`        | Ignore attribute changes |
| `replace_triggered_by`  | Force replacement        |
| `precondition`          | Validate before apply    |
| `postcondition`         | Validate after apply     |

---

# Variable Arguments

| Argument      | Description     |
| ------------- | --------------- |
| `type`        | Variable type   |
| `default`     | Default value   |
| `nullable`    | Allow null      |
| `sensitive`   | Hide value      |
| `validation`  | Validation rule |
| `description` | Documentation   |
| `ephemeral`   | Temporary value |

---

# Output Arguments

| Argument      | Description       |
| ------------- | ----------------- |
| `value`       | Output value      |
| `description` | Documentation     |
| `depends_on`  | Output dependency |
| `sensitive`   | Hide output       |
| `ephemeral`   | Temporary output  |

---

# Resource Provisioners

| Provisioner   | Description              |
| ------------- | ------------------------ |
| `local-exec`  | Run local command        |
| `remote-exec` | Run remote command       |
| `file`        | Copy file to remote host |

---

# Resource Connection Arguments

| Argument      | Description            |
| ------------- | ---------------------- |
| `host`        | Remote host            |
| `user`        | Username               |
| `password`    | Password               |
| `private_key` | SSH private key        |
| `port`        | Connection port        |
| `type`        | SSH or WinRM           |
| `timeout`     | Connection timeout     |
| `agent`       | Use SSH agent          |
| `script_path` | Remote script location |

---

# Common Expressions

| Expression          | Description            |
| ------------------- | ---------------------- |
| `condition ? a : b` | Conditional expression |
| `for`               | Loop expression        |
| `if`                | Filter in loop         |
| `...`               | Grouping operator      |
| `[*]`               | Full splat operator    |
| `[0]`               | Index access           |
| `.attribute`        | Attribute access       |

---

# Operators

| Operator | Description           |
| -------- | --------------------- |
| `+`      | Addition              |
| `-`      | Subtraction           |
| `*`      | Multiplication        |
| `/`      | Division              |
| `%`      | Modulus               |
| `==`     | Equal                 |
| `!=`     | Not equal             |
| `>`      | Greater than          |
| `<`      | Less than             |
| `>=`     | Greater than or equal |
| `<=`     | Less than or equal    |
| `&&`     | Logical AND           |
| `\|\|`   | Logical OR            |
| `!`      | Logical NOT           |

---

# Built-in Constants

| Constant | Description   |
| -------- | ------------- |
| `null`   | No value      |
| `true`   | Boolean true  |
| `false`  | Boolean false |

---

# Built-in Context Objects

| Object      | Description                   |
| ----------- | ----------------------------- |
| `var`       | Input variables               |
| `local`     | Local values                  |
| `path`      | Filesystem path information   |
| `terraform` | Terraform runtime information |
| `count`     | Current `count` index         |
| `each`      | Current `for_each` key/value  |
| `self`      | Current resource              |
| `module`    | Child module outputs          |

---

# Dynamic Blocks

| Block     | Description                             |
| --------- | --------------------------------------- |
| `dynamic` | Generate nested blocks programmatically |
| `content` | Body of generated block                 |

---

# Common CLI Commands

| Command               | Description                           |
| --------------------- | ------------------------------------- |
| `terraform init`      | Initialize working directory          |
| `terraform validate`  | Validate configuration                |
| `terraform fmt`       | Format configuration files            |
| `terraform plan`      | Generate execution plan               |
| `terraform apply`     | Apply changes                         |
| `terraform destroy`   | Destroy managed infrastructure        |
| `terraform show`      | Display state or plan                 |
| `terraform output`    | Show output values                    |
| `terraform state`     | Manage state                          |
| `terraform import`    | Import existing resources             |
| `terraform taint`     | Mark resource for recreation (legacy) |
| `terraform untaint`   | Remove taint (legacy)                 |
| `terraform graph`     | Generate dependency graph             |
| `terraform providers` | Show required providers               |
| `terraform version`   | Display Terraform version             |
| `terraform workspace` | Manage workspaces                     |
| `terraform login`     | Authenticate to Terraform Cloud       |
| `terraform logout`    | Remove Terraform Cloud credentials    |
| `terraform console`   | Interactive expression console        |
| `terraform test`      | Execute module tests                  |

# References
* [https://github.com/terraform-providers](https://github.com/terraform-providers)