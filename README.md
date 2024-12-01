
# docker-tags

A Bash script to fetch and display tags of a Docker image repository from Docker Hub or a custom registry.


## Features

- Executes API to fetch target repository tags.
- Supports docker hub and custom registeries.
- Supports fetching tags for official Docker images.
- Handles paginated responses seamlessly.
- Outputs total tag count.
- Optionally displays raw API responses.
- Customizable registry URL and pagination size.


## Requirements
- `bash` shell
- `curl`
- `jq` (automatically installed if missing)
## Installation

1. Clone the repository:
```bash
  git clone https://github.com/atamg/docker-tags.git
  cd docker-tags
```
2. Make the script executable:
```bash
  chmod +x docker-tags
```
3. (Optional) Add an alias to your shell:
```bash
  echo 'alias dt="path/to/docker-tags"' >> ~/.bashrc
  source ~/.bashrc
```
## Usage/Examples

```bash
./docker-tags [-o] [-r] <repository_name> [registry_url] [page_size]
```

1. Fetch tags for the official nginx image:
```bash
./docker-tags -o nginx
```
2. Fetch tags for a custom repository:
```bash
./docker-tags myrepo/myimage https://custom-registry.example.com
```
3. Output raw API responses for debugging:
```bash
./docker-tags -r -o nginx
```
4. Fetch tags for gitlab-ce
```bash
./docker-tags gitlab/gitlab-ce
```

## Output
- **Tags:** Lists all tags for the specified repository.
- **Total Count:** Displays the total number of tags found.


## Author

- Ata Mahmoudi [@atamg](https://www.github.com/atamq)


## License

[MIT](https://choosealicense.com/licenses/mit/)


