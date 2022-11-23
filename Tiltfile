def create_namespace(name):
    k8s_yaml(blob("""apiVersion: v1
kind: Namespace
metadata:
  name: %s
""" % name))

name = "local-path-provisioner-test"

create_namespace(name)

k8s_yaml(helm("charts/local-path-provisioner", name, namespace = name))
