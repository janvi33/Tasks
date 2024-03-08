from models import db
db.create_all()
from models import Task
from datetime import datetime
t = Task(title="xyz", date=datetime.utcnow())
t
db.session.add(t)
db.session.commit()


app.app_context().push()