# System.Transactions

``` diff
 namespace System.Transactions {
+    public sealed class DistributedTransactionPermission : CodeAccessPermission, IUnrestrictedPermission {
+        public DistributedTransactionPermission(PermissionState state);
+        public override IPermission Copy();
+        public override void FromXml(SecurityElement securityElement);
+        public override IPermission Intersect(IPermission target);
+        public override bool IsSubsetOf(IPermission target);
+        public bool IsUnrestricted();
+        public override SecurityElement ToXml();
+        public override IPermission Union(IPermission target);
+    }
+    public sealed class DistributedTransactionPermissionAttribute : CodeAccessSecurityAttribute {
+        public DistributedTransactionPermissionAttribute(SecurityAction action);
+        public new bool Unrestricted { get; set; }
+        public override IPermission CreatePermission();
+    }
 }
```

