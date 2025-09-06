

When running the command:

```bash
bazel run //:venv
```

## Bazel Run Errors by aspect_rules_py Version

### Version 1.6.3

You may encounter the following error:

```
Error:   × Unable to run command:
	├─▶ Failed to copy /home/ubuntu/.cache/bazel/
	│   _bazel_ubuntu/19a482a162c477d18f1125cc01d03ed4/sandbox/processwrapper-
	│   sandbox/63/execroot/_main/bazel-out/k8-fastbuild/bin/external/
	│   rules_python++pip+pip_312_opentelemetry_semantic_conventions/site-
	│   packages/opentelemetry/__init__.py to /home/ubuntu/.cache/bazel/
	│   _bazel_ubuntu/19a482a162c477d18f1125cc01d03ed4/sandbox/processwrapper-
	│   sandbox/63/execroot/_main/bazel-out/k8-fastbuild/bin/.venv/lib/
	│   python3.12/site-packages/opentelemetry/__init__.py
	╰─▶ Permission denied (os error 13)
```

### Version 1.5.2

The error may look like this:

```
Error:   × Unable to run command:
	╰─▶ Collision resolution not yet implemented! Saw opentelemetry/__init__.py
			twice
```

Note: This error also persists even if you set `package_collisions = "warning"`.

### Version 1.4.0

Everything works as expected with aspect_rules_py version 1.4.0.

```
Created virtualenv in /home/ubuntu/git/aspect_rules_py__mlflow__bug/.venv
```
