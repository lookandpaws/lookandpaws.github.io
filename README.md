### Local Build

- Change into the root directory of the project, followed by this:

```
$ bundle exec jekyll build
$ bundle exec jekyll serve
```

### Update Gem File Versions

- Change into the root directory of the project, followed by this:

```
$ bundle update
```

# How To Setup DNS
- Create a local file in the root directory called CNAME and add a single entry on line 1 as follows:

```
www.lookandpaws.com
```

- Navigate to Hover and create A records that point to each of the 4 IP addresses for GitHub Pages:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

- Following this, confirm that the A records are setup correctly using the dig command:

```
$ dig WWW.LOOKANDPAWS.COM +noall +answer
```

### Another DNS Configuration (that may not be necessary)
- Navigate to Hover and create a CNAME record that points to lookandpaws.github.io

---

### Confirm DNS Configured Correctly

- To confirm that your DNS record configured correctly, use the dig command:

```
$ dig WWW.LOOKANDPAWS.COM +nostats +nocomments +nocmd
```