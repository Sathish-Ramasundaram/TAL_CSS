
4. Tiny Goal: 

👉 Place Sidebar and Main side-by-side
You will learn:
display: flex
horizontal layout
width control

5. Update .layout

Replace with: 
.layout {
  border: 2px solid #ddd;
  margin: 20px;
  display: flex;
}


6. Test: 
Expected result
Sidebar and Main are now:

[ Sidebar ][ Main Content ]

----
display: flex makes children:
align in a row
share horizontal space
become flexible containers

7. Control sidebar width

To: 
.sidebar {
  background: #e5e7eb;
  padding: 20px;
  border: 1px solid #ccc;
  width: 220px;
}


8. Let main take remaining space

To: 
.main {
  padding: 20px;
  border: 1px solid #ccc;
  flex: 1;
}

---

flex: 1

“Take all remaining available space”

9. Test: 
Refresh
✅ Expected

Sidebar fixed width
Main fills remaining width
Layout feels like real dashboard

